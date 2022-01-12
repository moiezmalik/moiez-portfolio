<template>
  <div class="container">
    <div class="row pt-3 pb-5">
      <div class="col-md-6">
        <Button :title="'Back to Portfolios'" :link="'./'" :target="'_self'" />
      </div>
    </div>
    <div class="row">
      <div class="col-md-6">
        <img :src="portfolio.img" style="width: 100%" alt="portfolio image" />
      </div>
      <div class="col-md-6">
        <h1>{{ portfolio.title }}</h1>
        <p>{{ portfolio.description }}</p>
        <Button class="vist-project" :title="'Vist Project'" :target="'_blank'" :link="portfolio.link"/>
      </div>
    </div>
    <div class="row pt-5">
      <div class="col-md-12 portfolio-stats">
        <div class="row">
          <div class="col-md-3">
              <i class="fas fa-server socia-icons"></i>
              <h4>Category:</h4>
            <p>{{ portfolio.platform }}</p>
          </div>
          <div class="col-md-3">
              <i class="fas fa-cubes socia-icons"></i>
              <h4>Tech Stack:</h4>
            <p v-for="lang in portfolio.languages" :key="lang">
                {{ lang }}</p>
          </div>
          <div class="col-md-3">
              <i class="fas fa-calendar-check socia-icons"></i>
              <h4>Date:</h4>
              <p>{{portfolio.date}}</p>
          </div>
          <div class="col-md-3">
               <i class="fas fa-building socia-icons"></i>
              <h4>Company:</h4>
              <p>{{portfolio.company}}</p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";

export default {
  data() {
    return {
      portfolios: [],
      portfolio: {},
    };
  },
  async created() {
    const url = "http://moiezmalik.com/data/portfolios.json";
    try {
      const res = await axios.get(url);
      this.portfolios = res.data.portfolios;
      this.portfolio = await this.portfolios.filter((data) => {
        return data.id == this.$route.params.id;
      });
      this.portfolio = this.portfolio[0];
    } catch (err) {
      console.log(err);
    }
  },
  head() {
    return {
      title: this.portfolio.title,
      
      meta: [
      { charset: 'utf-8' },
      { name: 'viewport', content: 'width=device-width, initial-scale=1' },
        {
          hid: "description",
          name: "description",
          content: this.portfolio.description,
        },
      ],
    };
  },
};
</script>

<style scoped>
.container {
  padding-top: 100px;
}
h4{
    font-size: 18px;
    font-weight: bold;
}
h1 {
  font-family: "NunitoSans-Light";
}
p{
    margin-bottom: 0rem;
}
.vist-project{
    bottom: 0;
    position: absolute;
}
.portfolio-stats {
  padding: 30px 10px 10px 10px;
  border: 1px solid #f0b630;
  text-align: center;
}
.socia-icons{
    font-size: 45px;
    color: #f0b630;
    padding-bottom: 10px;
}
.socia-icons:hover{
    color: #ffff;
}
</style>>

<template>
  <div class="container">
    <div class="row">
      <div class="col-md-12 mb-3">
      <Button :title="'Back to Home'" :link="'/'" :target="'_self'"/>
      </div>
    </div>
      <div class="row">
          <Portfolios
            v-for="portfolio in portfolios"
            :key="portfolio.id"
            :title="portfolio.title"
            :description="portfolio.description"
            :link="portfolio.link"
            :img="portfolio.img"
            :platform="portfolio.platform"
            :languages="portfolio.languages"
            :id="portfolio.id"
          />
      </div>
    </div>
</template>

<script>
import axios from "axios";

export default {
    
    name: "index",
    data() {
    return {
      portfolios: [],
    };
  },
  async created() {
    const url = "http://moiezmalik.com/data/portfolios.json";
    try {
      const res = await axios.get(url);
      this.portfolios = res.data.portfolios.sort((a,b) => { return new Date(b.date) - new Date(a.date)});
    } catch (err) {
      console.log(err);
    }
  },
  head() {
    return {
      title: "Moiez Malik Projects",
      meta: [
        {
          hid: "description",
          name: "description",
          content: "View Moiez Malik recent projects and work",
        },
      ],
    };
  }

}
</script>

<style>

</style>
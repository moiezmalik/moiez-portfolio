<template>
  <div>
    <Banner />
    <SocialMedia />
    <div class="container">
      <div class="row">
        <div class="col-md-12 text-center pt-5 pb-5">
          <h3 class="project-title">Recent Projects</h3>
        </div>
      </div>
    </div>
    <div class="container">
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
    <div class="container projects-container">
      <div class="row">
        <div class="col-md-12 text-center">
          <Button :title="'More Projects'" :link="'/portfolios'" />
        </div>
      </div>
    </div>
    <div class="container-fluid experience-container">
      <div class="row text-center">
        <div class="col-md-4 offset-md-4">
          <h3 class="project-title pb-5">My Journey to be a Developer</h3>
        </div>
      </div>
      <div class="row">
        <Work />
      </div>
    </div>
    <div class="container-fluid text-center skills-container">
      <h3 class="pt-4 pb-5 project-title">Technical Skills</h3>
      <Skills />
    </div>
    <div class="container projects-container text-center">
      <h3 class="pt-4 pb-5 project-title">On my Spare Time</h3>
      <Hobbies />
    </div>
  </div>
</template>

<script>
import Portfolios from "~/components/portfolios/Portfolios.vue";
import axios from "axios";

export default {
  components: { Portfolios },
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
      this.portfolios = res.data.portfolios.sort((a,b) => { return new Date(b.date) - new Date(a.date)}).slice(0,6);
    } catch (err) {
      console.log(err);
    }
  },
  head() {
    return {
      title: "Moiez Malik Portfolio",
      meta: [
        
      { charset: 'utf-8' },
      { name: 'viewport', content: 'width=device-width, initial-scale=1' },
      {
          hid: "description",
          name: "description",
          content: "Moiez Malik portfolio and all my recent work",
          
        },
      ],
      link: [{ rel: 'icon', type: 'image/x-icon', href: '/favicon.ico' }]

    };
  },
};
</script>
<style>
.projects-container {
  padding-top: 125px;
  padding-bottom: 100px;
}
.experience-container {
  background-color: white;
  color: black;
  padding-top: 100px;
  background-image: url("http://moiezmalik.com/images/yellow-background.png");
  background-size: cover;
}
.project-title {
  display: inline-block;
  font-weight: bold;
  padding-top: 15px;
  border-top: 2px solid #f0b630;
  line-height: 1em;
  text-decoration: none;
}
.skills-container {
  padding-top: 100px;
  padding-bottom: 100px;
  background-image: url("https://www.counselservices.com/o/ipc-counsel-theme/images/hex%20pattern%20bg.png");
  background-size: cover;
  background-color: #16181b;
}
</style>
<template>
  <div class="col-md-4 mt-3">
    <nuxt-link class="portfolio-card-link" :to="'/portfolios/' + id">
      <div class="card" style="width: 100%">
        <div class="portfolio-img-container">
          <img :src="img" class="card-img-top" alt="portfolios image" />
          <div class="overlay"></div>
        </div>
        <div class="card-body">
          <h3 class="card-title">{{ title }}</h3>
          <p class="card-text">
            {{ description.replace(/^(.{60}[^\s]*).*/, "$1" + "...") }}
          </p>
          <p>Category:<strong> {{ platform }}</strong>
          </p>
        </div>
        <div class="card-footer"><span class="card-link portfolio-link">Learn More</span></div>
      </div>
    </nuxt-link>
  </div>
</template>

<script>
export default {
  name: "portfolios",
  props: ["title", "description", "link", "img", "platform", "languages", "id"],
};
</script>

<style scoped>
.portfolio-img-container {
  position: relative;
}
.overlay {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  display: block;
  background-color: rgba(0, 0, 0, 0.26);
}
.card:hover .overlay {
  display: none;
}
.card-img-top {
  min-height: 150px;
  max-height: 220px;
}
.portfolio-card-link,.portfolio-card-link:hover{
    color: white;
    text-decoration: none;
}
.card-title {
  padding-top: 15px;
}
h3 {
  font-size: 18px;
}
h2 {
  text-align: center;
}
.card {
  background-color: rgb(24, 24, 24);
  min-height: 400px;
  cursor: pointer;
}
.portfolio-link {
  color: #f0b630;
}
.portfolio-link:hover {
   font-weight: bold;
}
.card-title::before {
  background-color: #f0b630;
  content: "";
  display: inline-block;
  height: 2px;
  position: relative;
  vertical-align: middle;
  margin-right: 10px;
  width: 25px;
}
</style>
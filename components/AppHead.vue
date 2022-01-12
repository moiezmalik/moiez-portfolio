<template>
  <div class="container-fluid">
    <div class="row pt-4 pb-4 pt-md-5 pb-md-5">
      <div class="col-2 col-md-1 offset-md-7 text-center text-md-right">
        <a href="mailto:moiezmalik@live.ca" class="contact-link"
          ><i class="fas fa-envelope social-icons"></i
        ></a>
      </div>
      <div class="col-2 col-md-1 text-md-lefttext-center">
        <a href="tel:757-866-4104" class="contact-link"
          ><i class="fas fa-phone social-icons"></i
        ></a>
      </div>
      <div class="col-8 col-md-3 text-md-left text-center">
        <Button
          :title="'Download CV'"
          :link="'http://moiezmalik.com/resume.pdf'"
          :target="'_blank'"
        />
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.sticky {
  bottom: 0;
  position: absolute;
}
@media only screen and (min-width: 600px) {
  .col-md-3,
  .col-md-2 {
    text-align: right;
  }
}
@media only screen and (max-width: 600px) {
  .col-md-3,
  .col-md-2 {
    text-align: center;
    padding-top: 10px;
    padding-bottom: 10px;
  }
}

.container {
  padding-top: 30px;
}
.social-icons {
  font-size: 16px;
  color: #f0b630;
}

.contact-link {
  font-size: 16px;
  color: white;
  padding: 0px 20px 0px 5px;
}
.contact-link:hover {
  color: #f0b630;
  text-decoration: none;
}
</style>
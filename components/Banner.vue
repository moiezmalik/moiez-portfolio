<template>
  <div class="container-fluid">
    <div class="row">
    </div>
    <div class="row">
      <div class="col-md-6 text-center">
         <img class="moiez-img" src="http://moiezmalik.com/images/moiezmaliknew.jpeg" alt="Moiez Malik">
      </div>
        <div class="col-md-6 my-auto text-center">
          <h2>Welcome to my portfolio</h2>
          <h1>Moiez Malik</h1>
          <h3>Web Developer</h3>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>

.moiez-img{
    width: 100%;
}

h1{
    font-family: Licorice;
    font-size: clamp(3rem, 4.5vw, 5.5rem);
    text-decoration: underline #f0b630;
    text-underline-position: under;
    text-decoration-thickness: 2px;

}
h2{
    font-family: NunitoSans-Light;
    font-size: clamp(3rem, 4.5vw, 3.5rem);

}
</style>
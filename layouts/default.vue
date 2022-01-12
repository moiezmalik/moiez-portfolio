<template>
  <div>
    <div>
      <AppHead />
    </div>
    <main>
      <Nuxt />
    </main>
    <footer>
        <div>
          <p>Made with <i class="fas fa-heart" style="color: #f0b630"></i> by Moiez Malik</p>
        </div>
    </footer>
  </div>
</template>

<script>

export default {
  components: {
  },
  head(){
        return {
            title: 'Moiez Malik Portfolio',
            meta: [
                {
                    hid: 'description',
                    name: 'description',
                    content: 'Moiez Malik portfolio and all my recent work'
                }
            ],
            link: [
              {rel: "styleSheet", type:"text/css", href:"https://pro.fontawesome.com/releases/v5.10.0/css/all.css", integrity:"sha384-AYmEC3Yw5cVb3ZcuHtOA93w35dYTsvhLPVnYs9eStHfGJvOvKxVfELGroGkvsg+p", crossorigin:"anonymous"}
            ]
        }
    }
};
</script>

<style>
@font-face {
    font-family: 'Licorice';
    src: url('../static/fonts/Licorice-Regular.ttf');}
@font-face {
    font-family: 'NunitoSans-Light';
    src: url('../static/fonts/NunitoSans-Light.ttf');
}
p,a,span{
  font-family: 'NunitoSans-Light';
}

html{
   margin:0;
   padding:0;
   height:100%;
}
body {
   min-height:100%;
   position:relative;
   background-color: black;
   color: white;
   padding-bottom: 100px;
   font-family: 'NunitoSans-Light';
}
footer {
   position:absolute;
   bottom:0;
   width:100%;
   padding-top: 36px;   /* Height of the footer */
   text-align: center;
}
</style>
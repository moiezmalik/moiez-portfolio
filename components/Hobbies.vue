<template>
  <div class="row">
    <div class="col-md-4 pt-3">
      <div class="flip-box">
        <div class="flip-box-inner">
          <div class="flip-box-front">
            <img style="width: 300px;height:170px"
              src="http://moiezmalik.com/images/image0.png"
              alt="MoterCycle"
            />
          </div>

          <div class="flip-box-back">
            <p>
              Outside developmet I have strong passion in motercycles. Every
              summer to ride my motercycle Indian Scout Bobber Sixty (1000CC).
            </p>
          </div>
        </div>
      </div>
    </div>
    <div class="col-md-4 pt-3">
        <div class="flip-box">
        <div class="flip-box-inner">
          <div class="flip-box-front">
            <img style="width: 300px;height:170px"
              src="https://cdn.pocket-lint.com/r/s/970x/assets/images/154419-games-review-hands-on-playstation-5-hands-on-pics-image1-tbq3hzlrkw.jpg"
              alt="PS5"
            />
          </div>

          <div class="flip-box-back">
            <p>
              Sometimes I like to have video games nights with my family and friends. Playstation 5 has been my platform of choice in 2021. 
            </p>
          </div>
        </div>
      </div>
    </div>
    <div class="col-md-4 pt-3">
       <div class="flip-box">
        <div class="flip-box-inner">
          <div class="flip-box-front">
            <img style="width: 300px;height:170px"
              src="http://moiezmalik.com/images/pc-build.jpg"
              alt="PC"
            />
          </div>

          <div class="flip-box-back">
            <p>
              I enjoy working on hardware as much as software. This is my 2020 built (i7 8700 with 1060 ghaphic card and 1TB M2).   
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style>
.flip-box {
  background-color: transparent;
  width: 300px;
  height: 170px;
  perspective: 1000px;
  margin: 0 auto;
}

.flip-box-inner {
  position: relative;
  width: 100%;
  height: 100%;
  text-align: center;
  transition: transform 0.8s;
  transform-style: preserve-3d;
}

.flip-box:hover .flip-box-inner {
  transform: rotateY(180deg);
}

.flip-box-front,
.flip-box-back {
  position: absolute;
  width: 100%;
  height: 100%;
  -webkit-backface-visibility: hidden;
  backface-visibility: hidden;
}

.flip-box-front {
  background-color: #bbb;
  color: black;
}

.flip-box-back {
  background-color: #f0b630;
  color: black;
  transform: rotateY(180deg);
  padding: 10px;
}
</style>
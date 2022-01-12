<template>
  <div class="container-fluid">
    <div class="row">
      <div class="col-md-3 pl-xl-5">
        <div class="pt-3">
          <h4><span class="yellow-number">1</span> Computer Programming</h4>
          <div style="padding-left: 32px;">
          <h5>Sheridan College</h5>
          <p>
            Focus: Building interactive-user application, web server Apache,
          </p>
          </div>
        </div>
        <div class="pt-3">
          <h4><span class="yellow-number">2</span> Web Developer</h4>
          <div style="padding-left: 32px;">
          <h5>Investment Planning Counsel</h5>
          <p>
            Built and managed over 350 website for independant financial advisors.
          </p>
          </div>
        </div>
         <div class="pt-3">
          <h4><span class="yellow-number">3</span> Marketing Tech Specialist</h4>
          <div style="padding-left: 32px;"> 
            <h5>Investment Planning Counsel</h5>
            <p>
                Build and manage corporate applications and websites. Support new initiative to recruit advisors and bring over $2B in Assets.   
            </p>
          </div>
        </div>
      </div>
      <div class="col-md-6">
        <img class="road-img" src="http://moiezmalik.com/images/road.png" alt="journey" />
      </div>
      <div class="col-md-3 pr-xl-5">
        <div class="pt-3">
          <h4><span class="yellow-number">4</span> Angular/Vue/NodeJs</h4>
          <div style="padding-left: 32px;">
          <h5>Plural Sight</h5>
          <p>
            Over 120 hours of self-learning in Angular 8+, Vue Js and Node Js. 
          </p>
          </div>
        </div>
        <div class="pt-3">
          <h4><span class="yellow-number">5</span> Bachelor of Computing Science</h4>
          <div style="padding-left: 32px;">
          <h5>Thompson Rivers University</h5>
          <p>
            Focus: Artificial Intelligence, Software Architecture and Design, Computer Programming, Mobile Development, Database System
          </p>
          </div>
        </div>
        <div class="pt-3">
          <h4><span class="yellow-number">6</span> React</h4>
          <div class="d-left-p">
          <h5>Plural Sight</h5>
          <p>
            By end of 2022 self-learn advance React and build application in React to showcase the study.
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

<style scoped>
@media (min-width: 1400px){
    .pl-xl-5, .px-xl-5 {
        padding-left: 3rem !important;
    }
}
@media (min-width: 1119px){
    .d-left-p {
        padding-left: 32px;
    }
}
@media (max-width: 769px){
    .d-left-p {
        padding-left: 32px;
    }
}
.road-img {
  width: 100%;
}
.yellow-number {
  color: black;
  font-weight: bold;
  border-radius: 16px;
  padding: 3px 8px 3px 8px;
  background-color: #f0b630;
}
h4 {
  font-size: min(max(16px), 5vw);
  font-weight: bold;
}
h5 {
  font-size: min(max(16px), 5vw);
  font-weight: bold;
}
p{
  font-size: min(max(15px), 5vw);
}
.experience-textbox {
  text-align: left;
}
</style>
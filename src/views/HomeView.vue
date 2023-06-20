<template>
    <div class="home">
  
      <LandingPage msg="Welcome to Your Vue.js App"/>
      <span class="landing-highlight a"> &#160; Phillip Kim</span>
            <span class="landing-highlight b" >Full Stack Developer</span>
    </div>
  </template>
  
  <script>
  // @ is an alias to /src
  import LandingPage from '../components/LandingPage.vue'
  
  export default {
    name: 'HomeView',
    components: {
      LandingPage
    }
  }
  </script>
  
  <style scoped>
  
  .landing-highlight {
    position: absolute;
    font-family: 'Arvo', serif;
    font-size: clamp(55px, 20vw, 90px);
    font-weight: 250;
    line-height: 1.3;
    z-index: 9999;
  }
  .landing-highlight.a {
    -webkit-transform: translate(-40px, -710px);
            transform: translate(-40px, -710px);
            right: 700px;
  }
  
  .landing-highlight.b {
    -webkit-transform: translate(-20px, -710px);
            transform: translate(-20px, -710px);
            left: 600px;
            bottom: -450px;
  }
  
  .landing-highlight.b,
  .landing-highlight.a {
    color: #c5efff;
  }
  
  </style>
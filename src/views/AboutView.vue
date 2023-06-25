<template>
    <div class="about">
      <h1 class = "title">About Me</h1>
      <a href="https://linkedin.com/in/phillipy-kim" target="_blank">
      <img class = "title-img" src="/Images/profile.jpg" alt="self-photo">
    </a>
      <p class = "about-summary" style="color: rgb(206, 206, 105)">Hey there! I'm Phillip, and I've always been captivated by the thrill of problem-solving and the excitement of learning new skills. During my university days, I focused on Human Computer Interaction, driven by a desire to uncover the best solutions for user-centered design. However, along the way, I stumbled upon the world of software development.

As I dived into the realms of HTML, CSS, and JavaScript, a passion ignited within me. I can vividly recall the moments when I created my very first portfolio website, crafted entirely from scratch. Sure, it may not have been the most visually stunning design, but that feeling of accomplishment was unbeatable.

As of now, I have successfully completed an incredible Full Stack Development Bootcamp with Tech Elevator. I wholeheartedly dedicated myself to enhancing my proficiency in both Backend and Frontend development. As a result, I expanded my skill set by seamlessly integrating Backend Java, utilizing PostgreSQL, and honing my abilities on the Frontend using Vue.js. The Bootcamp has equipped me with a well-rounded expertise in building robust web applications from end to end.</p>
    </div>
  </template>
  <style scoped>

  .about {
    min-height: 100vh;
    background-color: #232323;
    padding: 50px;
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
    justify-content: flex-start;
    margin-bottom: 120px;
  }
  .title {
    color: #FF0;
    height: 100px;
  }
  .title-img {
    border-radius: 50%;
    height: 250px;
    margin-bottom: 100px;
    transition: filter 0.3s ease;
  }
  .title-img:hover {
    filter: grayscale(100%) blur(0.5px);
  }

  .about-summary {
    padding: 30px 120px;
    word-wrap: break-word; 
}
  </style>
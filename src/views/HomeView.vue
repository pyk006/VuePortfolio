<template>
    <div class="home">
      <span class="typed-text">{{ typeValue }}</span>

      <LandingPage class = "landing"/>

    </div>
  </template>
  
  <script>
  // @ is an alias to /src
  import LandingPage from '../components/LandingPage.vue'
  
  export default {
    name: 'HomeView',
    components: {
      LandingPage
    },
    data: () => {
    return {
      typeValue: "",
      displayTextArray: ["Phillip Kim", "Full Stack", "UI/UX"],
      typingSpeed: 100,
      erasingSpeed: 100,
      newTextDelay: 500,
      displayTextArrayIndex: 0,
      charIndex: 0,
    };
  },
  methods: {
    typeText() {
      if (this.charIndex < this.displayTextArray[this.displayTextArrayIndex].length) {
        if (!this.typeStatus) this.typeStatus = true;
        this.typeValue += this.displayTextArray[this.displayTextArrayIndex].charAt(
          this.charIndex
        );
        this.charIndex += 1;
        setTimeout(this.typeText, this.typingSpeed);
      } else {
        this.typeStatus = false;
        setTimeout(this.eraseText, this.newTextDelay);
      }
    },
    eraseText() {
      if (this.charIndex > 0) {
        if (!this.typeStatus) this.typeStatus = true;
        this.typeValue = this.displayTextArray[this.displayTextArrayIndex].substring(
          0,
          this.charIndex - 1
        );
        this.charIndex -= 1;
        setTimeout(this.eraseText, this.erasingSpeed);
      } else {
        this.typeStatus = false;
        this.displayTextArrayIndex += 1;
        if (this.displayTextArrayIndex >= this.displayTextArray.length)
          this.displayTextArrayIndex = 0;
        setTimeout(this.typeText, this.typingSpeed + 1000);
      }
    },
  },
  created() {
   setTimeout(this.typeText, this.newTextDelay + 200);
},
  }
  </script>
  
  <style lang = "scss" scoped>
  
.home {
  position: relative;

}
.typed-text {
  text-shadow: 2px 2px 4px rgba(255, 0, 0, 0.5);
  position: absolute;
  display: flex;
  justify-content: center;
  align-items: center;
  top: 40%;
  left: 50%;
  transform: translate(-50%, -50%);
  color: rgb(255, 255, 188);
  font-size: 8rem;
}


@media only screen and (max-width: 1023px) {
  .typed-text {
    font-size: 5rem;
  }
}

@media only screen and (max-width: 767px) {
  .typed-text {
    font-size: 3rem;
  }
}

@media only screen and (max-width: 479px) {
  .typed-text {
    font-size: 2rem;
  }
}

  
  </style>
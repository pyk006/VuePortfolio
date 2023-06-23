<template>
    <div class="home">
      <span class="typed-text">{{ typeValue }}</span>

      <LandingPage/>


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
      typeStatus: false,
      displayTextArray: ["Phillip Kim", "Full Stack", "UI/UX"],
      typingSpeed: 100,
      erasingSpeed: 100,
      newTextDelay: 2000,
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
  

.typed-text {
  position: absolute;
  top: 55%;
  left: 50%;
  transform: translate(-50%, -50%);
}

.typed-text {
  color: #c3e1ff;
  font-size: 10rem;
}

  
  </style>
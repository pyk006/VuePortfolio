<template>
        <h1 class = "project-header" style="color: #FF0">
            Projects
            <div class = "grid">
              
              <a class = "grid-item grid-animal" href="https://github.com/pyk006/T.E.-Paws-Rescue" target="_blank">
                <img class = "card-image animal-shelter" src="/Images/TEPaws.PNG" alt="shelter-website">
                <div class="overlay">
          <h3>T.E. Paws Rescue</h3>
          <p>A Full Stack Animal Shelter Application, using Java w/ Spring, PostgreSQL, and Vue.js</p>
        </div>
              </a>
              <a class = "grid-item grid-tenmo" href="https://github.com/crystallyyy/Tenmo" target="_blank">
                <img class = "card-image tenmo" src="/Images/Tenmo.PNG" alt="tenmo-app">
                <div class="overlay">
          <h3>Tenmo</h3>
          <p>A Backend Server-side Money Transfer Application using Java Spring and PostgreSQL</p>
        </div>
              </a>
              <a class = "grid-item grid-vending" href="https://github.com/pyk006/Vending-Machine" target="_blank">
                <img class = "card-image vending-machine" src="/Images/Vending.PNG" alt="vending-machine-app">
                <div class="overlay">
          <h3>Vending Machine</h3>
          <p>A Backend Vending Machine CLI Application using Java</p>
        </div>
              </a>
              <a class = "grid-item grid-gym" href="https://github.com/nikkih95159/Gym-Pal" target="_blank">
                <img class = "card-image gym-pal" src="/Images/Gym.PNG" alt="gym-pal-app">
                <div class="overlay">
          <h3>Gym-Pal</h3>
          <p>A Front-End Gym Assistance Application using HTML, CSS, JavaScript w/ Bootstrap</p>
        </div>
              </a>
              <a class = "grid-item grid-yum" href="https://www.figma.com/proto/EYtt0E4ENxZlbZdrDxLgtx/MegaYum?node-id=136-0&starting-point-node-id=136%3A0" target="_blank">
                <img class = "card-image mega-yum" src="/Images/Megayum.PNG" alt="mega-yum-prototype">
                <div class="overlay">
          <h3>MegaYum</h3>
          <p>A prototype nutrition AR application using Figma (UX Design Project)</p>
        </div>
              </a>
              <a class = "grid-item grid-data" href="https://github.com/pyk006/ROT13-Encoder" target="_blank">
                <img class = "card-image rot-13" src="/Images/ROT13.PNG" alt="rot-13-cli">
                <div class="overlay">
          <h3>ROT-13 Encoder</h3>
          <p>A Backend Java CLI ROT-13 Encoder</p>
        </div>
              </a>
          </div>

        </h1>

</template>

<script>

export default {
  name: 'ProjectsView',
  components: {
  },
}
</script>
<style scoped>
    * {
        background-color: #232323;
    }
    .project-header {
        margin: 0;
        padding: 50px 0px;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        color: #c5efff;
    }
    .grid {
      height: auto;
      padding: 30px;
      display: grid;
      grid-template-columns: 1fr 1fr 1fr;
      grid-template-areas: "animal tenmo vending"
                            "gym yum data";
      row-gap: 50px;
      column-gap: 120px;
      justify-items: center;
    }
    .grid-item {
      height: 40vh;
      width: 40vh;
      border-radius: 5px;
      border: 2px solid rgb(230 225 239);
      cursor: pointer;
      transition: transform 0.3s ease, box-shadow 0.3s ease;

    }
    .grid-item:hover {
      box-shadow: -6px 6px 10px rgba(255,255,0,0.5), 6px 6px 10px rgba(255,255,0,0.5), 0 6px 10px rgba(255,255,0,0.5);
      transform: scale(1.02);

    }
    .grid-animal {
      grid-area: "animal";

    }
    .grid-tenmo {
      grid-area: "tenmo";
    }
    .grid-vending {
      grid-area: "vending";
    }
    .grid-gym {
      grid-area: "gym";
    }
    .grid-yum {
      grid-area: "yum";
    }
    .grid-data {
      grid-area: "data";
    }
    .card-image {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }
  .vending-machine, .rot-13 {
    object-position: left;
  }
  .gym-pal {
    object-position: center;
  }
  .mega-yum {
    object-position: center;
  }
  @media only screen and (max-width: 767px) {
  .grid {
    grid-template-columns: 1fr;
    grid-template-areas: "animal"
                          "tenmo"
                          "vending"
                            "gym" 
                            "yum" 
                            "data";
  }
}
.overlay {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    opacity: 0;
    transition: opacity 0.3s ease;
    background-color: rgba(0, 0, 0, 0.7);
    color: #fff;
    padding: 1rem;
    text-align: center;
    pointer-events: none;
  }
  .overlay h3,
  .overlay p {
    background-color: transparent;
  }
  .overlay p {
    font-size: 15px;
  }

  .grid-item:hover .overlay {
    opacity: 1;
    pointer-events: auto;
  }
</style>
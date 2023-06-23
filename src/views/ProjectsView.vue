<template>
        <h1 class = "project-header">
            Projects
            <div class = "grid">
              <a class = "grid-item grid-animal" href="https://github.com/pyk006/T.E.-Paws-Rescue" target="_blank">
                <img class = "card-image animal-shelter" src="/Images/TEPaws.PNG" alt="shelter-website">
              </a>
              <a class = "grid-item grid-tenmo" href="https://github.com/crystallyyy/Tenmo" target="_blank">
                <img class = "card-image tenmo" src="/Images/Tenmo.PNG" alt="tenmo-app">
              </a>
              <a class = "grid-item grid-vending" href="https://github.com/pyk006/Vending-Machine" target="_blank">
                <img class = "card-image vending-machine" src="/Images/Vending.PNG" alt="vending-machine-app">
              </a>
              <a class = "grid-item grid-gym" href="https://github.com/nikkih95159/Gym-Pal" target="_blank">
                <img class = "card-image gym-pal" src="/Images/Gym.PNG" alt="gym-pal-app">
              </a>
              <a class = "grid-item grid-yum" href="https://www.figma.com/proto/EYtt0E4ENxZlbZdrDxLgtx/MegaYum?node-id=136-0&starting-point-node-id=136%3A0" target="_blank">
                <img class = "card-image mega-yum" src="/Images/Megayum.PNG" alt="mega-yum-prototype">
              </a>
              <a class = "grid-item grid-data" href="https://github.com/pyk006/ROT13-Encoder" target="_blank">
                <img class = "card-image rot-13" src="/Images/ROT13.PNG" alt="rot-13-cli">
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
        background-color: #061428;
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
      box-shadow: -6px 6px 10px rgba(223, 17, 17, 0.5), 6px 6px 10px rgba(223, 17, 17, 0.5), 0 6px 10px rgba(223, 17, 17, 0.5);
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
</style>
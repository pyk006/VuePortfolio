<template>
        <h1 class = "project-header">
            Projects
            <div class = "grid">
              <div class = "grid-item grid-animal" @click="githubRedirect"></div>
              <div class = "grid-item grid-tenmo" @click="githubRedirect"></div>
              <div class = "grid-item grid-vending" @click="githubRedirect"></div>
              <div class = "grid-item grid-gym" @click="githubRedirect"></div>
              <div class = "grid-item grid-yum" @click="githubRedirect"></div>
              <div class = "grid-item grid-data" @click="githubRedirect"></div>
          </div>

        </h1>

</template>

<script>

export default {
  name: 'ProjectsView',
  components: {
  },
  methods: {
    githubRedirect (e) {
      if (e.target.classList.contains('grid-animal')) {
        window.open('https://github.com/pyk006/T.E.-Paws-Rescue', '_blank');
      }
      if (e.target.classList.contains('grid-tenmo')) {
        window.open('https://github.com/crystallyyy/Tenmo', '_blank');
      }
      if (e.target.classList.contains('grid-vending')) {
        window.open('https://github.com/pyk006/Vending-Machine', '_blank');
      }
      if (e.target.classList.contains('grid-gym')) {
        window.open('https://github.com/nikkih95159/Gym-Pal', '_blank');
      }
      if (e.target.classList.contains('grid-yum')) {
        window.open('https://www.figma.com/proto/EYtt0E4ENxZlbZdrDxLgtx/MegaYum?node-id=136-0&starting-point-node-id=136%3A0', '_blank');
      }
      if (e.target.classList.contains('grid-data')) {
        window.open('https://github.com/pyk006/ROT13-Encoder', '_blank');
      }
    }
  }
}
</script>
<style scoped>
    * {
        background-color: #061428;
        height: 100vh;
    }
    .project-header {
        margin: 0;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        color: #c5efff;
    }
    .grid {
      padding: 30px;
      display: grid;
      grid-template-columns: 1fr 1fr 1fr;
      grid-template-areas: "animal tenmo vending"
                            "gym yum data";
      column-gap: 120px;
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
</style>
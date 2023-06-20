<template>
        <h1 class = "project-header">
            Projects
            <ProjectsPage/>
            <projects-carousel/>
        </h1>

</template>

<script>
import ProjectsCarousel from '../components/ProjectsCarousel.vue'
// @ is an alias to /src
import ProjectsPage from '../components/ProjectsPage.vue'

export default {
  name: 'ProjectsView',
  components: {
    ProjectsPage,
    ProjectsCarousel
  }
}
</script>
<style scoped>
    * {
        background-color: #061428;
        height: 100vh;
    }
    .project-header {
        display: flex;
        flex-direction: column;
        color: #c5efff;
    }
</style>
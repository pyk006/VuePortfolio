<template>
    <div>
        <h1 class = "project-header">
            Projects
        </h1>
        <ProjectsPage/>
    </div>
</template>

<script>
// @ is an alias to /src
import ProjectsPage from '../components/ProjectsPage.vue'

export default {
  name: 'ProjectsView',
  components: {
    ProjectsPage
  }
}
</script>
<style scoped>
    * {
        background-color: #061428;
        height: 100vh;
    }
    .project-header {
        color: #c5efff;
    }
</style>
<template>
  <div class = "main">
    
  <nav class = "nav-bar">
    <div class="logo__main" @click="refreshPage">
      <svg
              version="1.1"
              id="logo"
              xmlns="http://www.w3.org/2000/svg"
              xmlns:xlink="http://www.w3.org/1999/xlink"
              x="20px"
              y="20px"
              viewBox="0 0 595.28 841.89"
              style="enable-background: new 0 0 595.28 841.89"
              xml:space="preserve"
            >

              <path
                class="logo-letter"
                d="M363.42,292.17c0,56.4-40,90-106.4,90h-47.2v-38.8h48.4c40.8,0,61.2-18.4,61.2-50.8c0-33.6-22-50.4-61.2-50.4h-48.4v-40.4h47.2C323.42,201.77,363.42,233.77,363.42,292.17z M191,242.17v-40.4h-44v280h44v-99.6v-38.8V242.17z"
              />
            </svg>
          </div>
          <div class = "nav-links">
    <router-link class = "router" to="/" key="home">Home</router-link> |
    <router-link class = "router" to="/about" key="about">About</router-link>
    <router-link class = "router" to="/projects" key="projects">Projects</router-link>
  </div>
  </nav>
  <transition name="fade" mode="out-in">
      <router-view/>
    </transition>
  <footer class = "footer">
    <ul class = "footer-list">
      <li><a class = "mailto" href="mailto:phillipkim777@gmail.com">Contact Me!</a></li>
    </ul>
  </footer>
</div>
</template>
<script>
import router from '@/router/index';
export default {
  methods: {
    refreshPage() {
      this.$route.path != '/' ? router.push('/') : window.location.reload();

    }

	},
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;


}
::-webkit-scrollbar {
  width: 1.2em;
}

::-webkit-scrollbar-track {
  background: #232323;
}

::-webkit-scrollbar-thumb {
  background: rgb(173, 173, 7);
  border-radius: 100vw;
  border: 0.35em solid #232323;
}

::-webkit-scrollbar-thumb:hover {
  background: rgb(82, 90, 13);
}

.nav-bar {
  display: flex;
  position: relative;
  justify-content: space-between;
  padding: 10px;
  background-color:#232323;
  box-shadow: 0 0.1rem 1rem rgba(255, 255, 0, 0.7);
  z-index: 1;
}
.nav-links {
  display: flex;
}

.nav-links router-link {
  display: inline-block;
  font-weight: bold;
  color: rgb(102, 102, 66);

  padding: 0 10px;
}

nav a {
  display: inline-block;
  font-weight: bold;

  color: rgb(102, 102, 66);
  padding-top: 30px;
  padding-right: 60px;
}

nav a.router-link-exact-active {
  color: #FF0;
}
.footer {
  padding: 20px;
  box-shadow: 0 0.3rem 1.5rem #FF0;
  background-color: #232323;
}
.footer-list {
  text-align: right;
}
.footer-list li {
  list-style: none;
}
.mailto {
  border: 1px solid rebeccapurple;
  padding: 15px;
  text-decoration: none;
  color: #FF0;
}
.logo-letter {
  cursor: pointer;
  fill: #FF0;
  width: 10px;

}
.logo-letter:hover {
  fill: #FF0;
}
.logo__main {
  height: 90px;
  width: 70px;
  flex-shrink: 0;
}
#logo:hover {
  cursor: pointer;
}
#logo:hover .logo-letter {
  fill: rgb(119, 119, 83);
}

.router {
  text-decoration: none;
}
.main {
  background: #232323;
  will-change: transform, opacity;
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s ease-out;
}

</style>

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
    <router-link class = "router" to="/" key="home">Home</router-link> |
    <router-link class = "router" to="/about" key="about">About</router-link>
    <router-link class = "router" to="/projects" key="projects">Projects</router-link>
  </nav>
  <router-view v-slot="{ Component }">
    <transition :name="anim" mode="out-in">
      <Component :is="Component"/>
    </transition>
  </router-view>
  <footer class = "footer">
    <ul class = "footer-list">
      <li><a class = "mailto" href="mailto:phillipkim777@gmail.com">Contact Me!</a></li>
    </ul>
  </footer>
</div>
</template>
<script>
export default {
  methods: {
    refreshPage() {
      window.location.reload();
    }

	},
  data() {
		return {
			anim: 'fade'
		};
  }
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
  background: #061428;
}

::-webkit-scrollbar-thumb {
  background: #819fbe;
  border-radius: 100vw;
  border: 0.35em solid #061428;
}

::-webkit-scrollbar-thumb:hover {
  background: #0270c4;
}

.nav-bar {
  display: flex;
  position: relative;
  justify-content: flex-end;
  padding: 10px;
  background-color:#061428;
  box-shadow: 0 0.5rem 1rem rgba(85, 159, 194, 0.6);
  z-index: 1;
}

nav a {
  display: inline-block;
  font-weight: bold;

  color: #35697e;
  padding-top: 30px;
  padding-right: 60px;
}

nav a.router-link-exact-active {
  color: #c5efff;
}
.footer {
  padding: 20px;
  box-shadow: 0 0.3rem 0.5rem rgb(85, 159, 194);
  background-color: #061428;
  z-index: 9999;
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
  color: #c5efff;
}
.logo-letter {
  cursor: pointer;
  fill: rgb(188, 211, 236);
  width: 10px;

}
.logo-letter:hover {
  fill: rgba(188, 211, 236, 0.5);
}
.logo__main {
  padding-right: 1500px;
  height: 90px;
  width: 70px;
  flex-shrink: 0;
}
#logo:hover {
  cursor: pointer;
}
#logo:hover .logo-letter {
  fill: rgba(188, 211, 236, 0.5);
}

.router {
  text-decoration: none;
}
.main {
  will-change: transform, opacity;
}
.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.5s ease-out
}

</style>

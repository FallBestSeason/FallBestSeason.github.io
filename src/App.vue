<template>
  <NavBar @navButtonClick="navButtonClick"/>
  <component :is="currentComponent"></component>
</template>

<script>
import NavBar from './components/NavBar.vue'
import Home from './components/Home.vue'
import Projects from './components/Projects.vue'
import Blog from './components/Blog.vue'
import Contact from './components/Contact.vue'
import 'bootstrap/dist/css/bootstrap.min.css'

export default {
  name: 'App',
  components: {
    NavBar,
    Home,
    Projects,
    Blog,
    Contact
  },
  data() {
    return {
      currentPage: 0,
      componentList: [Home, Projects, Blog, Contact]
    }
  },
  computed: {
    currentComponent() {
      return this.componentList[this.currentPage]
    }
  },
  methods: {
    navButtonClick(pageIndex) {
      this.currentPage = pageIndex
    }
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
  margin-top: 0px;
}
</style>

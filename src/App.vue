<template>
  <NavBar @navButtonClick="navButtonClick"/>
  <component :is="currentComponent"></component>
</template>

<script>
import NavBar from './components/NavBar.vue'
import Home from './components/Home.vue'
import Projects from './components/Projects.vue'
import Contact from './components/Contact.vue'
import 'bootstrap/dist/css/bootstrap.min.css'

export default {
  name: 'App',
  components: {
    NavBar,
    Home,
    Projects,
    Contact
  },
  data() {
    return {
      currentPage: 0,
      componentList: [Home, Projects, Contact]
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
html, body {
  height: 100%;
  margin: 0;
  padding: 0;
}
#app {
  height: 100%;
  font-family: 'Courier New', Courier, monospace;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #95fbff;;
  margin-top: 0px;
  background-color: #5f9ea0;
  font-size: large;
}
.cCen {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 70vh;
    text-align: left;
    flex-wrap: wrap;
    gap: 10px;
  }
.cItem {
  flex: 1 1 200px;
  padding: 10px;
}
.hContainer {
  display: flex;
  align-items: center;
  gap: 10px;
}
.hItem {
  flex: 1 1 200px;
}
.cBox {
  padding: 10px;
}
.cBackBtn {
  margin-top: 10px;
  margin-right: 10px;
}
.cNavBar {
  display: flex;
  justify-content: space-between;
  width: 100%
}
</style>

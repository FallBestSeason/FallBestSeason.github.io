<template>
  <h2>projects</h2>
  <component :is="currentComponent"></component>
</template>

<script>
import ProjectTiles from './projectPages/ProjectTiles.vue';

export default {
  name:'ProjectsPage',
  components: {
    ProjectTiles
  },
  data() {
    return {
      currentPage: 0,
      componentList: [ProjectTiles]
    }
  },
  computed: {
    currentComponent() {
      return this.componentList[this.currentPage]
    }
  }
}
</script>

<style scoped>
.cTile {
  width: 400px;
  padding: 10px;
}

.cardImage {
  height: 140px;
  width: 100px;
}
</style>
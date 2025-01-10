<template>
  <component :is="currentProject" @projectTileClick="projectTileClick"/>
</template>

<script>
import ProjectTiles from './projectPages/ProjectTiles.vue';
import ThisWebsite from './projectPages/ThisWebsite.vue';

export default {
  name:'ProjectsPage',
  components: {
    ProjectTiles,
    ThisWebsite
  },
  data() {
    return {
      currentPage: 0,
      componentList: [ProjectTiles, ThisWebsite]
    }
  },
  computed: {
    currentProject() {
      return this.componentList[this.currentPage]
    }
  },
  methods: {
    projectTileClick(pageIndex) {
      if (pageIndex >= this.componentList.length - 1) {
        this.currentPage = 0
      } else {
        this.currentPage = pageIndex + 1
      }
    }
  }
}
</script>

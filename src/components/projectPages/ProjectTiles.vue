<template>
  <div class="cCen">
    <div 
      v-for="(card, index) in cards" :key="index" 
      @click="projectTileClick(index)" 
      class="hContainer cTile bg-dark"
    >
      <img class="cImage hItem" :src="card.image" alt="thumbnail loading..."/>
      <div class="hItem">
        <h3>{{ card.title }}</h3>
        <p>{{ card.description }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name:'ProjectTiles',
  data() {
    return {
      cards: [
        {
          image: "/projectTileAssets/siteLogo.png",
          title: "This Website",
          description: "tech stack breakdown",
        },
        {
          image: "/projectTileAssets/fillerIcon.png",
          title: "More Coming Soon",
          description: "",
        }
      ]
    }
  },
  methods: {
    projectTileClick(pageIndex) {
      this.$emit('projectTileClick', pageIndex);
    }
  }
}
</script>

<style scoped>
.cTile {
  width: 400px;
  padding: 10px;
}

.cImage {
  height: 140px;
  width: 100px;
  object-fit: contain;
}
</style>

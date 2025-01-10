<template>
  <div class="bg-dark text-white p-3 c-navbar">
    <button class="c-navbar-label" @click="buttonClick(0)">aut0's site</button>
    <div class="right-section">
      <button
        v-for="(button, index) in buttons" :key="index"
        :class="{ 'active': index === currentPage }"
        @click="buttonClick(index)"
        class="c-btn-spacing"
      >
        {{ button.text }}
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name:'NavBar',
  data() {
    return {
      currentPage: 0,
      buttons: [
        {
          id: 0,
          text: "Home",
        },
        {
          id: 0,
          text: "Projects",
        },
        {
          id: 0,
          text: "Blog",
        },
        {
          id: 0,
          text: "Contact",
        }
      ]
    }
  }, 
  methods: {
    buttonClick(pageIndex) {
      this.currentPage = pageIndex
      this.$emit('navButtonClick', pageIndex);
    }
  }
}
</script>

<style scoped>
.c-btn-spacing {
  margin-right: 5px
}
.c-navbar {
  display: flex;
  justify-content: space-between;
  width: 100%
}
.c-navbar-label {
  margin-right: 20px
}
.right-section {
  display: flex;
  align-items: center
}
.active {
  background-color: rgb(177, 177, 185);
}
</style>
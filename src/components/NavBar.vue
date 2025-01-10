<template>
  <div class="bg-dark text-white p-3 c-navbar">
    <button class="c-navbar-label">aut0's site</button>
    <div class="right-section">
      <button @click="buttonClick(0)" class="c-btn-spacing">home</button>
      <button @click="buttonClick(1)" class="c-btn-spacing">projects</button>
      <button @click="buttonClick(2)" class="c-btn-spacing">blog</button>
      <button @click="buttonClick(3)">contact</button>
    </div>
  </div>
</template>

<script>
export default {
  name:'NavBar',
  methods: {
    buttonClick(pageIndex) {
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
  pointer-events: none;
  margin-right: 20px
}
.right-section {
  display: flex;
  align-items: center
}
</style>
<template>
  <div class="bg-dark text-white p-3 cNavBar">
    <button class="cNavBarLabel" @click="buttonClick(0)">aut0's site</button>
    <div class="navBtnContainer">
      <button
        v-for="(button, index) in buttons" :key="index"
        :class="{ 'active': index === currentPage }"
        @click="buttonClick(index)"
        class="cNavBtnSpacing"
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
          text: "home",
        },
        {
          id: 0,
          text: "projects",
        },
        {
          id: 0,
          text: "contact",
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
.cNavBtnSpacing {
  margin-right: 5px
}
.cNavBarLabel {
  margin-right: 20px
}
.navBtnContainer {
  display: flex;
  align-items: center
}
.active {
  background-color: rgb(177, 177, 185);
}
</style>
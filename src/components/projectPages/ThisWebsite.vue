<template>
  <div class="cNavBar">
    <div></div>
    <button class="cBackBtn" @click="backButtonClick">back to projects</button>
  </div>
  <div class="cCen cTextWrap">
    <p class="bg-dark cBox">
    site is written in
    <a href="https://vuejs.org/">vue.js</a>
    and deployed using
    <a href="https://pages.github.com/">github pages</a>
    <br><br>
    you can view the source code on my
    <a href="https://github.com/FallBestSeason/FallBestSeason.github.io">github</a><br>
    it's free to use under the MIT license
    <br><br>
    I chose to use vue.js for my framework because of a few factors<br>
    I wanted to try keeping the whole site as a single page,<br>
    as I had not used this design paragdigm before.<br>
    Vue is an excellent choice for this, learning the design structure was<br>
    very easy because of the simplicity of the component system.
    <br><br>
    if you're looking to make a similar site,<br>
    I would strongly reccomend it
  </p>
  </div>
</template>

<script>
export default {
  name:'ThisWebsitePage',
  methods: {
    backButtonClick() {
      this.$emit('projectTileClick', Number.MAX_SAFE_INTEGER);
    }
  }
}
</script>

<style scoped>
.cTextWrap {
  flex: 1 1 200px;
  padding: 10px;
  white-space: pre-wrap;
}
</style>
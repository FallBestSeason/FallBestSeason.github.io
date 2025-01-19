<template>
  <div class="cCen text-light">
    <img class="cHeadshot bg-dark cBox" src="/homeAssets/headshot.jpg" alt="headshot loading..."/>
    <p class="bg-dark cBox cHomeText">
      hello! I'm autumn or aut0, a programmer / IT professional / massive bike nerd based out of southeast MI
      <br><br>
      this site contains a portfolio of projects and contact information if you need to reach me
      <br><br>
      I wrote the site from scratch using vue.js<br>
      you can find out more about it under the projects tab.
      <br><br>
      if you can read this I am looking for work! <br>
      please check out the projects tab and grab my resume from the contact tab!
    </p>
  </div>
</template>

<script>
export default {
  name:'HomePage'
};
</script>

<style scoped>
.cHeadshot {
  margin-top: 10px;
  height: 60vh;
  width: 40%;
  object-fit: cover;
}
.cHomeText {
  text-align: left;
  width: 50%;
  margin-top: 10px;
}
</style>

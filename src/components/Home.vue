<template>
  <div class="cen text-light">
    <img class="cHeadshot bg-dark cBox" src="/headshot.jpg" alt="headshot loading..."/>
    <p class="bg-dark cBox cText">
      hello! I'm autumn or aut0, a programmer / IT professional / massive bike nerd based out of southeast MI
      <br><br>
      This site contains a portfolio of projects, a blog, and contact information if you need to reach me
      <br><br>
      I wrote the site from scratch in javascript using vue.js<br>
      I didn't use any pre-existing templates or icons, so all of the effects are 100% in-house
      <br><br>
      If you can read this I am looking for work! Please find my resume attached in the contact tab!<br>
    </p>
  </div>
</template>

<script>
export default {
  name:'HomePage'
};
</script>

<style scoped>
.cBox {
  padding: 10px;
}
.cHeadshot {
  height: 80%;
  width: 40%;
  object-fit: cover;
}
.cText {
  text-align: justify;
  width: 50%;
}
</style>
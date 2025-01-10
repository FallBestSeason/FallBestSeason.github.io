<template>
  <div class="cCen">
    <div class="text-light bg-dark c-bg-pad">
      <div class="cItem">Contact me:</div>
      <div class="cItem">Email: <a href="mailto:024.aut@gmail.com">024.aut@gmail.com</a></div>
      <div class="cItem">Github: <a href="https://github.com/FallBestSeason">FallBestSeason</a></div>
      <div class="cItem hContainer">Resume: 
        <div class="hItem">
          <a href="/resume2025.pdf" target="_blank" rel="noopener noreferrer">.PDF </a>
        </div>
        <div class="hItem">
          <a href="/resume2025.rtf" target="_blank" rel="noopener noreferrer">.RTF </a>
        </div>
        <div class="hItem">
          <a href="/resume2025.docx" target="_blank" rel="noopener noreferrer">.DOCX</a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name:'ContactPage',
  props: {
    msg: String
  }
}
</script>
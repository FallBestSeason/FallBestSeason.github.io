<template>
  <div class="cen">
    <div class="text-light bg-dark c-bg-pad">
      <div class="item">Contact me:</div>
      <div class="item">Email: <a href="mailto:024.aut@gmail.com">024.aut@gmail.com</a></div>
      <div class="item">github: <a href="https://github.com/FallBestSeason">FallBestSeason</a></div>
      <div class="item">Documents:</div>
      <div class="item">Resume: 
        <div class="item">
          <button><a href="/resume2025.pdf" target="_blank" rel="noopener noreferrer">.PDF </a></button>
          <a href="/resume2025.rtf" target="_blank" rel="noopener noreferrer">.RTF </a>
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
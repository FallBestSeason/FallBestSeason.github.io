<template>
  <h1>blog - coming soon</h1>
  <ul class="list-group cCen">
    <li class="list-group-item">item1</li>
    <li class="list-group-item">item2</li>
    <li class="list-group-item">item3</li>
  </ul>
  <div v-html="renderedMarkdown"></div>
</template>

<script>
import MarkdownIt from "markdown-it";
const markdown = new MarkdownIt();

export default {
  name: 'BlogPage',
  data() {
    fileContent: ''
  },
  computed: {
    renderedMarkdown() {
      return markdown.render(fileContent);
    }
  },
  watch: {
    markdownFilePath: {
      async handler(newFilePath) {
        try {
          const fileContent = await fs.readFile(newFilePath, "utf8");
          this.renderedMarkdown = markdown.render(fileContent);
        } catch (err) {
          console.error(err);
        }
      },
      immediate: true
    }
  }
}
</script>

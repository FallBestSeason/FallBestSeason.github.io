<template>
  SITE IS A WORK IN PROGRESS!
  <div class="cen text-light">
    <div v-if="fileContent">
      <pre class="bg-dark c-bg-pad">{{ fileContent }}</pre>
    </div>
    <div v-else>
      <p>Loading file content...</p>
    </div>
  </div>
  
</template>

<script>
export default {
  name:'HomePage',
  data() {
    return {
      fileContent: null,
    };
  },
  mounted() {
    this.loadFileContent();
  },
  methods: {
    async loadFileContent() {
      try {
        const response = await fetch('/intro.txt');
        if (!response.ok) {
          throw new Error('Failed to fetch file');
        }
        const text = await response.text();
        this.fileContent = text;
      } catch (error) {
        console.error(error);
        this.fileContent = 'Error loading file.';
      }
    }
  }
};
</script>
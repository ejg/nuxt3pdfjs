<template>
  <div ref="viewer"></div>
</template>

<script>
/* eslint-disable */
import WebViewer from '@pdftron/pdfjs-express-viewer';

export default {
  name: 'WebViewer',
  mounted: function () {
    WebViewer(
      {
        path: 'lib/',
        initialDoc: `files/demo.pdf`,
        licenseKey: 'VMeLR5MsW5lX3X9YfqQF',
      },
      this.$refs.viewer
    ).then((instance) => {
      // then
    });
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
div {
  width: 100%;
  height: 100vh;
}
</style>

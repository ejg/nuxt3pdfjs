<template>
  <div ref="viewer"></div>
</template>

<script>
export default {
  name: 'WebViewer',
  mounted: function () {
    import('@pdftron/pdfjs-express-viewer').then(() => {
      WebViewer(
        {
          path: 'lib/',
          initialDoc: `files/demo.pdf`,
          licenseKey: 'VMeLR5MsW5lX3X9YfqQF',
        },
        this.$refs.viewer
      ).then((instance) => {
        // call apis here
      });
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

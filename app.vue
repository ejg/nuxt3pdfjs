<template>
  <div id="app">
    <WebViewer />
    <!-- <WebViewerNoWindow /> -->
  </div>
</template>

<script>
import WebViewer from './components/WebViewer.vue';

export default {
  name: 'app',
  components: {
    WebViewer,
  },
  data() {
    return {
      publicPath: process.env.BASE_URL,
    };
  },
};
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>

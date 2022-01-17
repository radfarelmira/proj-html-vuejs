<template>
  <div id="app">
    <Header />

    <main>
      Main
    </main>

    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";

export default {
  name: "App",
  components: {
    Header,
    Footer
  },
};
</script>

<style lang="scss">
@import './style/general.scss';
@import './style/variables.scss';
</style>

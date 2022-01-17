<template>
  <div id="app">
    <Header :headerToplinksArray="headerTopLinks" :headerTopIconsArray="headerTopIcons" :headerBottomLinksArray="headerBottomLinks"/>

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
  data: function() {
    return {
      headerTopLinks: [
        {
         text:'home',
         url: '#'
        },
        {
         text:'pages',
         url: '#'
        },
        {
         text:'course formats',
         url: '#'
        },
        {
         text:'courses',
         url: '#'
        },
        {
         text:'Demos',
         url: '#'
        }
      ],
      headerTopIcons: [
        {
          class: 'fab fa-facebook',
          url: 'https://it-it.facebook.com/'
        },
        {
          class: 'fab fa-twitter',
          url: 'https://twitter.com/?lang=it'
        },
        {
          class: 'fab fa-instagram',
          url: 'https://www.instagram.com/'
        },
        {
          class: 'fab fa-linkedin',
          url: 'https://it.linkedin.com/'
        },
        {
          class: 'fab fa-google-plus',
          url: '#'
        },
        {
          class: 'fab fa-youtube',
          url: 'https://youtube.com/'
        },
      ],
      headerBottomLinks: [
        {
          text: 'business',
          class: 'fas fa-chart-bar',
          url: '#'
        },
        {
          text: 'design',
          class: 'fas fa-palette',
          url: '#'
        },
        {
          text: 'development',
          class: 'fas fa-cog',
          url: '#'
        },
        {
          text: 'lifestyle',
          class: 'far fa-smile',
          url: '#'
        },
        {
          text: 'office productivity',
          class: 'fas fa-chart-line',
          url: '#'
        },
      ]
    }
  }
};
</script>

<style lang="scss">
@import './style/general.scss';
@import './style/variables.scss';
</style>

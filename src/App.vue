<template>
  <div id="app">
    <Header :headerToplinksArray="headerTopLinks" :headerTopIconsArray="headerTopIcons" :headerBottomLinksArray="headerBottomLinks"/>

    <main>
      <Banner />

      <DevelopmentCourses :developmentCoursesArray="developmentCuorses"/>
    </main>

    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";
import Banner from "./components/Banner.vue";
import DevelopmentCourses from "./components/DevelopmentCourses.vue";

export default {
  name: "App",
  components: {
    Header,
    Footer,
    Banner,
    DevelopmentCourses
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
      ],
      developmentCuorses: [
        {
          src: require('./assets/img/13.jpg'),
          text: 'The Complete IOS 10 &amp; Swift 3 Developer Courses',
          raiting: 4,
          exPrice: '$199.99',
          discount: '$100'
        },
        {
          src: require('./assets/img/3.jpg'),
          text: 'Web Design for Beginners: Real World Coding in HTML &amp; CSS',
          raiting: 5,
          exPrice: '$129.99',
          discount: '$65'
        },
        {
          src: require('./assets/img/9.jpg'),
          text: 'GitHub Ultimate: Master Git and GitHub - Beginner to Expert ',
          raiting: 4,
          exPrice: '$99.99',
          discount: '$50'
        },
        {
          src: require('./assets/img/25.jpg'),
          text: 'The Complete IOS 11 &amp; Swift Developer Courses - Build 20 Apps',
          raiting: 4,
          exPrice: '$199.99',
          discount: '$100'
        },
        {
          src: require('./assets/img/15.jpg'),
          text: 'Android Java Masterclass - Become an App Developer',
          raiting: 4,
          exPrice: '$99.99',
          discount: '$50'
        },
        {
          src: require('./assets/img/19.jpg'),
          text: 'Xamarin Forms: Build Native Cross-platform Apps with C#',
          raiting: 4,
          exPrice: '$109.99',
          discount: '$95'
        }
      ]
    }
  }
};
</script>

<style lang="scss">
@import './style/general.scss';
@import './style/variables.scss';
</style>

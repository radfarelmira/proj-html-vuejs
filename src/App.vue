<template>
  <div id="app">
    <Header :headerToplinksArray="headerTopLinks" :headerTopIconsArray="headerTopIcons" :headerBottomLinksArray="headerBottomLinks"/>

    <main>
      <Banner />

      <DevelopmentCourses :developmentCoursesArray="developmentCuorses"/>

      <Jumbotron />

      <RecentCourses :recentCoursesLinksArray="recentCoursesLinks" :recentCoursesArray="recentCourses"/>

      <Subscribe />

      <PopularCourses :allCoursesArray="recentCourses"/>

      <Activities />

      <Testimonial />
    </main>

    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";
import Banner from "./components/Banner.vue";
import DevelopmentCourses from "./components/DevelopmentCourses.vue";
import Jumbotron from "./components/Jumbotron.vue";
import RecentCourses from "./components/RecentCourses.vue";
import Subscribe from "./components/Subscribe.vue";
import PopularCourses from "./components/PopularCourses.vue";
import Activities from "./components/Activities.vue";
import Testimonial from "./components/Testimonial.vue";

export default {
  name: "App",
  components: {
    Header,
    Footer,
    Banner,
    DevelopmentCourses,
    Jumbotron,
    RecentCourses,
    Subscribe,
    PopularCourses,
    Activities,
    Testimonial
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
      ],
      recentCoursesLinks: ['all categories', 'business', 'design', 'development', 'IT & software', 'lifestyle','marketing', 'office productivity'],
      recentCourses: [
        {
          title: 'Development >',
          src: require('./assets/img/13.jpg'),
          text: 'The Complete IOS 10 &amp; Swift 3 Developer Courses',
          raiting: 4,
          exPrice: '$199.99',
          discount: '$100'
        },
        {
          title: 'Design >',
          src: require('./assets/img/29.jpg'),
          text: 'CSS - The Complete Guide 2020 (incl, Flexbox, Grid &amp; Sass)',
          raiting: 5,
          exPrice: '$199.99',
          discount: '$100'
        },
        {
          title: 'Development >',
          src: require('./assets/img/3.jpg'),
          text: 'Web Design for Beginners: Real World Coding in HTML &amp; CSS',
          raiting: 5,
          exPrice: '$129.99',
          discount: '$65'
        },
        {
          title: 'Design >',
          src: require('./assets/img/23.jpg'),
          text: 'Digitally Painting Light and Color: Amateur to Master',
          raiting: 4,
          exPrice: '$139.99',
          discount: '$70'
        },
        {
          title: 'Art & Crafts >',
          src: require('./assets/img/1.jpg'),
          text: 'Become an Arabic Calligraphy Artist from Scratch',
          raiting: 4,
          discount: '$50'
        },
        {
          title: 'Google >',
          src: require('./assets/img/31.jpg'),
          text: 'Google Searching Ninja!',
          raiting: 3,
          exPrice: '$89.99',
          discount: '$45'
        },
        {
          title: 'Art & Crafts >',
          src: require('./assets/img/17.jpg'),
          text: 'Foundation for Mastering Watercolor',
          raiting: 4,
          exPrice: '$19.99',
          discount: '$10'
        },
        {
          title: 'Food & Beverage >',
          src: require('./assets/img/5.jpg'),
          text: 'FGet Wine-Smart',
          raiting: 4,
          exPrice: '$49',
          discount: '$25'
        },
        {
          title: 'Art & Crafts >',
          src: require('./assets/img/7.jpg'),
          text: 'The Colored Pencil Drawing Cuorse',
          raiting: 4,
          exPrice: '$34.99',
          discount: '$18'
        },
        {
          title: 'Art & Crafts >',
          src: require('./assets/img/11.jpg'),
          text: 'Paint Realistic Watercolor and Botanicals - STUDIO BASICS',
          raiting: 4,
          exPrice: '$69.99',
          discount: '$35'
        },
        {
          title: 'Art & Crafts >',
          src: require('./assets/img/27.jpg'),
          text: 'Mastering Brushstrokes - Part 1',
          raiting: 5,
          exPrice: '$19.99',
          discount: '$10'
        },
        {
          title: 'Art & Crafts >',
          src: require('./assets/img/21.jpg'),
          text: 'Paint Realistic Watercolour and Botanicals - MAGNOLIAS',
          raiting: 5,
          exPrice: '$69.99',
          discount: '$35'
        },
      ],
    }
  }
};
</script>

<style lang="scss">
@import './style/general.scss';
@import './style/variables.scss';
</style>

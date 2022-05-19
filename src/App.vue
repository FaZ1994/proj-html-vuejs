<template>
  <div id="app">
    <header>
      <header-component />
    </header>
    <main>
      <hero-component />
      <contacts-a-component />
      <call-us-component />
      <courses-component />
      <our-stats />
      <instructor-component/>
      <testimonial-component/>
      <latest-news-component/>
      <news-letter-component />
    </main>

      <footer-component />
  </div>
</template>

<script>
import FooterComponent from "./components/FooterComponent.vue";
import HeaderComponent from "./components/HeaderComponent.vue";
import ContactsAComponent from "./components/ContactsAComponent.vue";
import HeroComponent from "./components/HeroComponent.vue";
import CallUsComponent from "./components/CallUsComponent.vue";
import CoursesComponent from "./components/CoursesComponent.vue";
import OurStats from './components/OurStats.vue';
import InstructorComponent from './components/InstructorComponent.vue';
import TestimonialComponent from './components/TestimonialComponent.vue';
import NewsLetterComponent from './components/NewsLetterComponent.vue';
import LatestNewsComponent from './components/LatestNewsComponent.vue';


export default {
  name: "App",
  components: {
    HeaderComponent,
    ContactsAComponent,
    FooterComponent,
    HeroComponent,
    CallUsComponent,
    CoursesComponent,
    OurStats,
    InstructorComponent,
    TestimonialComponent,
    NewsLetterComponent,
    LatestNewsComponent,
  },
};
</script>

<style lang="scss">
@import "./styles/general.scss";

/* #app{
 font-family: $main-font;
} */
</style>

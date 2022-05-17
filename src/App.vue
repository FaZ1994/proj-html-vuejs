<template>
  <div id="app">
    <header>
      <header-component />
    </header>
    <main>
      <main-component />
    </main>
    <footer>
      <footer-component />
    </footer>
  </div>
</template>

<script>
import FooterComponent from "./components/FooterComponent.vue";
import HeaderComponent from "./components/HeaderComponent.vue";
import MainComponent from "./components/MainComponent.vue";

export default {
  name: "App",
  components: {
    HeaderComponent,
    MainComponent,
    FooterComponent,
  },
};
</script>

<style lang="scss">
@import "./styles/general.scss";
</style>

<template>
    <section class="hero">
      <div class="container">
        <div class="row">
          <div class="col-12">
            <h1>Drive with Avada</h1>
            <h2>We offer the finest driving tuition money can buy</h2>
          </div>
        </div>
      </div>
    </section>
</template>


<script>
export default {
  name: "HeroComponent",
  components: {},
};
</script>

<style lang="scss" scoped>
@import "../styles/general.scss";

.hero {
  height: 550px;
  margin-top: -115px;
  background-image: url("../assets/img/homepage-hero-background.jpg");
  background-size: cover;
  background-position: center;

  & div {
    height: 100%;
    color: $white;
    display: flex;
    flex-direction: column;
    justify-content: center;
  }

  & h1 {
    font-size: 4em;
    font-weight: 500;
  }

  & h2 {
    font-size: 1.5em;
    font-weight: 400;
  }
}

</style>

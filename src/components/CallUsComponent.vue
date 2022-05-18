<template>
  <section class="call-us-sect">
    <div class="container">
      <div class="row">
        <div class="col-8">
          <h2>Start Learning to Drive Today</h2>
          <h3>Give us a call to schedule your first driving lesson</h3>
        </div>
        <div class="col-4 d-flex align-items-center">
          <i class="fa-solid fa-phone fa-rotate-270 fa-xl mx-4"></i>
          <span>1-800-555-555</span>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "CallUsComponent",
  components: {},
  data() {
    return {};
  },
};
</script>

<style lang="scss">
@import "../styles/general.scss";

.call-us-sect {
  background-image: url("../assets/img/horizontal-cta-background.jpg");
  background-size: cover;
  padding: 60px 0;
  color: $white;

  h2 {
    font-weight: 500;
    font-size: 40px;
    line-height: 1.5;
  }

  h3 {
    font-weight: 500;
    font-size: 20px;
    line-height: 1.5;
  }

  span {
    font-weight: 500;
    font-size: 30px;
    line-height: 1.5;
    display: inline-block;
  }
}
</style>

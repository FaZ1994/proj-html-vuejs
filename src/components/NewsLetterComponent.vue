<template>
  <section class="newsletter">
    <div class="container">
      <div class="row text text-center">
        <div class="col-8 offset-2">
          <h2>Sign up to our Newsletter</h2>
          <form class="form-group">
            <input type="email" name="email" />
            <button type="submit" class="btn-green">Subscribe</button>
          </form>
          <p>
            (We do not share your data with anybody, and only use it for its
            intended purpose)
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "NewsLetterComponent",
  components: {},
};
</script>

<style lang="scss" scoped>
@import "../styles/general.scss";

.newsletter {
  background-image: url("../assets/img/newsletter_background.jpg");
  background-size: cover;
  padding: 60px 0;

  h2 {
    font-size: 30px;
    color: $gray-dark;
    margin-bottom: 50px;
  }

  p {
    font-size: 14px;
    color: $gray-transp;
  }

  input {
    font-size: 14px;
    border-radius: 4px;
    height: 50px;
    width: 80%;
    margin: auto;
    margin-bottom: 30px;
    border: 1px solid $gray-transp;
    background-color: $white;
    padding: 0 20px;

    &:focus {
      outline: none;
    }
  }

  button {
    width: 80%;
    margin: auto;
    margin-bottom: 20px;
  }
}
</style>

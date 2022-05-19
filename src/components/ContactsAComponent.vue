<template>
    <section class="contacts-area">
      <div class="container">
        <div class="row">
          <div class="col-lg-6 description">
            <h2>Get Behind The Wheel</h2>
            <p>
              Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc
              ultrices auctor sapien id cursus. Aliquam maximus turpis in
              vehicula semper.
            </p>
            <p>
              Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc
              ultrices auctor sapien id cursus. Aliquam maximus turpis in
              vehicula semper. Fusce et ultrices libero, at suscipit lacus. Sed
              vitae fringilla nibh. Nunc ultrices auctor sapien id cursus.
              Aliquam maximus turpis in vehicula semper. Fusce et ultrices
              libero, at suscipit lacus. Sed vitae fringilla nibh.
            </p>
          </div>
          <div class="col-lg-6 contact-form">
            <div class="text-center">
              <h3>First Lesson Free!</h3>
              <p>
                When you make a block booking with us your first lesson is
                included free.
              </p>
              <form class="form-group" action="index.html" method="post">
                <input
                  type="text"
                  class="form-control"
                  name="name"
                  placeholder="Your Name*"
                  minlength="5"
                />
                <input
                  type="email"
                  class="form-control"
                  name="email"
                  placeholder="Email*"
                  minlength="5"
                />
                <input
                  type="text"
                  class="form-control"
                  name="phone"
                  placeholder="Telephone"
                  minlength="5"
                />
                <input
                  type="text"
                  class="form-control"
                  name="location"
                  placeholder="Location"
                  minlength="5"
                />
                <button type="submit" class="btn-green" name="button">
                  request a callback
                </button>
              </form>
            </div>
          </div>
        </div>
      </div>
    </section>
 
</template>

<script>
export default {
  name: "MainComponent",
  components: {},
};
</script>

<style lang="scss" scoped>
@import "../styles/general.scss";

.contacts-area {
  padding-top: 80px;
  margin-top: 0px;
  padding-right: 30px;
  margin-bottom: 0px;
  padding-left: 30px;

  .description {
    h2 {
      font-size: 40px;
      color: $gray-dark;
      margin-bottom: 31px;
    }
    p {
      color: $gray-transp;
      font-size: 21px;
      line-height: 2;
      font-weight: 400;

      &:last-of-type {
        font-size: 16px;
      }
    }
  }

  .contact-form {
    & > div {
      border-radius: 10px;
      padding: 40px;
      background-color: $white;
      box-shadow: $gray-transp 0px 25px 20px 0px;
      position: relative;
      top: -110px;
      margin-bottom: 80px;
    }

    h3 {
      font-size: 30px;
      color: $green-main;
      margin-bottom: 40px;
    }

    p {
      font-size: 16px;
      color: $gray-transp;
      margin-bottom: 40px;
    }

    input {
      margin-bottom: 28px;
      height: 50px;
      background-color: $white;

      &:focus {
        outline: none;
        box-shadow: none;
        border-color: $gray-transp;
      }

      &::placeholder {
        font-size: 12px;
        color: $gray-transp;
      }
    }
  }
}
</style>

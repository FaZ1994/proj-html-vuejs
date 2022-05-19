<template>
  <section class="instructors">
    <div class="container">
      <div class="row">
        <div class="col-8">
          <h2>Your Instructors</h2>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc
            ultrices auctor sapien id cursus. Aliquam maximus turpis in vehicula
            semper.
          </p>
        </div>
        <div class="col-4 align-self-center">
          <button class="btn-green">More about us</button>
        </div>
      </div>
    </div>

    <div class="container-lg">
      <div class="row no-gutters">
        <div class=" col-4">
          <div class="instructor-container">
            <div class="instructor text-center">
              <div>
                <img
                  src="../assets/img/instructor-mikehart.jpg"
                  alt="mikehart"
                />
                
              </div>
              <h3>Mike Hart</h3>
              <div class="social">
                <a href="#"><i class="fa-brands fa-facebook-f"></i></a>
                <a href="#"><i class="fa-brands fa-twitter"></i></a>
                <a href="#"><i class="fa-brands fa-instagram"></i></a>
              </div>
              <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
            </div>
          </div>
        </div>
        <div class=" col-4">
          <div class="instructor-container">
            <div class="instructor text-center">
              <div>
                <img
                  src="../assets/img/instructor-johnsmith.jpg"
                  alt="johnsmith"
                />
                
              </div>
              <h3>John Smith</h3>
              <div class="social">
                <a href="#"><i class="fa-brands fa-facebook-f"></i></a>
                <a href="#"><i class="fa-brands fa-twitter"></i></a>
                <a href="#"><i class="fa-brands fa-instagram"></i></a>
              </div>
              <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
            </div>
          </div>
        </div>
        <div class=" col-4">
          <div class="instructor-container">
            <div class="instructor text-center">
              <div>
                <img
                  src="../assets/img/instructor-angelahart.jpg"
                  alt="angelahart"
                />
                
              </div>
              <h3>Angela Hart</h3>
              <div class="social">
                <a href="#"><i class="fa-brands fa-facebook-f"></i></a>
                <a href="#"><i class="fa-brands fa-twitter"></i></a>
                <a href="#"><i class="fa-brands fa-instagram"></i></a>
              </div>
              <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "InstructorComponent",
  components: {},
};
</script>

<style lang="scss" scoped >
@import "../styles/general.scss";

.instructors {
  position: relative;
  margin-bottom: 0;
  padding-bottom: 100px;
  z-index: 1;
  button {
    width: 100%;
  }

  .container:first-of-type {
    margin-bottom: 80px;
  }

  h3 {
    font-size: 24px;
    font-weight: 700;
    line-height: 1.5;
    color: $gray-dark;
    margin: 20px 0 10px;
  }

  p {
    color: $black-transp-04;
    line-height: 2;
  }

  .container:first-of-type p {
    font-size: 21px;
  }

  .container:last-of-type p {
    margin-bottom: 20px;
  }

  img {
    width: 100%;
    transition: all 0.3s ease-in-out;

    &:hover {
      transform: scale(1.05);
      box-shadow: 0 3px 15px $black-transp-04;
    }
  }

  & > div {
    position: relative;
  }

  .instructor-container {
    background-color: $green-main;
    border-radius: 12px;
    box-shadow: $black-transp-01 0px 25px 20px 0px;
    margin: 0 7px;
  }

  .instructor {
    background-color: $white;
    border-radius: 5px 5px 12px 12px;
    height: 100%;
    border: none;
    position: relative;
    top: 6px;
    padding: 40px;

  }

  & > div.container-lg > div > div:nth-child(2) > div {
    margin: 5px 0;
  }

  .container:last-of-type {
    position: absolute;
    left: 50%;
    transform: translate(-50%, -50%);
    bottom: -320px;
  }

  & > div:nth-child(2) > div > div:nth-child(2) > div > div {
    padding-bottom: 55px;
  }

  .fa-brands {
    font-size: 18px;
    color: $black-transp-04;
    margin: 0 10px;
  }

  .social {
    margin-bottom: 10px;

  }
}
</style>

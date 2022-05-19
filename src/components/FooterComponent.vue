<template>
  <footer>
    <section class="contacts-details">
      <div class="container">
        <div class="row align-items-center">
          <div class="col-3">
            <a href="#"
              ><img
                class="logo"
                src="../assets/img/avada-drivers-logo-1x.png"
                alt="avada logo"
            /></a>
            <p>
              Avada Driving School is the right choice for experienced drivers
              looking for a refresher course, or the brand new driver wanting to
              pass first time.
            </p>
          </div>
          <div class="col-3">
            <h3 class="text-uppercase">contacts details</h3>
            <ul class="list-group list-unstyled">
              <li class="d-block d-flex">
                <i class="d-none d-lg-inline fa-solid fa-home"></i>
                12345 North Main Street, New York, NY 555555
              </li>
              <li>
                <i class="d-none d-lg-inline fa-solid fa-phone fa-rotate-270"></i>
                1.800.555.6789
              </li>
              <li>
                <i class="d-none d-lg-inline fa-solid fa-envelope"></i>
                info@your-domain.com
              </li>
              <li>
                <i class="d-none d-lg-inline fa-solid fa-link"></i>
                Theme-Fusion.com
              </li>
            </ul>
          </div>
          <div class="col-3">
            <h3 class="text-uppercase">courses</h3>
            <ul class="list-group list-unstyled">
              <li
                v-for="(link, index) in footerLinks"
                class="courses"
                :key="index"
              >
                <i
                  class="far fa-arrow-alt-circle-right icon-green d-none d-lg-inline"
                ></i>
                <a href="#">{{ link }}</a>
              </li>
            </ul>
          </div>
          <div class="col-3 d-flex flex-column align-items-center">
            <img
              src="../assets/img/footer-ad-grid-200x178.png"
              class="img-fluid pb-3"
              alt=""
            />

            <button class="btn-green">
              {{ footerButton }}
            </button>
          </div>
        </div>
      </div>
    </section>

    <section class="credits">
      <div class="container">
        <div class="row">
          <div class="col-9">
            <p>
              © Copyright 2012 - 2020 | Avada Theme by
              <a class="h-ref" href="#">ThemeFusion</a>
              | All Rights Reserved | Powered by
              <a class="h-ref" href="https://github.com/FaZ1994"
                >FaZ1994</a
              >
            </p>
          </div>
          <div class="col-3">
            <div class="social">
              <a href="#"><i class="fa-brands fa-facebook-f"></i></a>
              <a href="#"><i class="fa-brands fa-twitter"></i></a>
              <a href="#"><i class="fa-brands fa-youtube"></i></a>
              <a href="#"><i class="fa-brands fa-instagram"></i></a>
            </div>
          </div>
        </div>
      </div>
    </section>
  </footer>
</template>

<script>
export default {
  name: "FooterComponent",
  components: {},
  data() {
    return {
      footerLinks: [
        "Pass Plus",
        "Intensive Course",
        "Automatic",
        "Instructor Training",
      ],
      footerButton: "book now",
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../styles/general.scss";

.contacts-details {
  background-image: url("../assets/img/footer-background-color.jpg");
  background-size: cover;
  padding: 70px 0;

  p {
    font-size: .8em;
    line-height: 2;
    font-weight: 400;
    color: $gray-light-transp-04
  }

  img.logo {
    max-width: 80%;
    margin-bottom: 20px;
  }

  h3 {
    font-size: 16px;
    font-weight: 700;
    color: $white;
  }

  ul li {
    color:$gray-light-transp-04;
    font-size: 13px;
    margin: 5px 0;
  }

  i {
    color: $gray-light;
    font-size: 17px;
    margin-right: 10px;
  }

  a {
    font-size: 16px;
    font-weight: 500;
    color: $green-main;
    transition: all 0.2s ease-in-out;

    &:hover {
      color: $green-sec;
    }
  }

  li {
    .icon-green {
      color: $green-main;
    }

    &.courses {
      margin: 2px 0;

      a {
        text-decoration: none;
      }
    }
  }
}

.credits {
  background-color: $black;
  padding: 30px 0;
  color: $gray-dark;
  font-size: 12px;
  padding: 50px 0;

  .h-ref {
    color: $green-main;
  }

  .social a {
    color: $white;
    font-size: 16px;
    margin: 0 10px;
    transition: all 0.2s ease-in-out;
  }

  a:hover {
    text-decoration: none;
    color: $green-sec;
  }

  p {
    margin: 0;
    line-height: 24px;
  }

  .social {
    margin-top: 15px;
  }
}
</style>

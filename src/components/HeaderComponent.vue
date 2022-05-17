<template>
  <section>
    <!-- CONTACTS -->
    <section class="contacts">
      <div class="container">
        <div class="row">
          <div class="col-lg-6">
            <span>We have a 95% Successful Pass Rate!</span>
          </div>
          <div class="col-lg-6 text-lg-end">
            <span>
              <i class="fa-solid fa-phone px-2"></i>
              Give us a call to book your tuition! 1-800-555-555
            </span>
          </div>
        </div>
      </div>
    </section>

    <!-- HEADER -->
    <header>
      <div class="container-lg">
        <div class="row align-items-center">
          <div class="col-lg-4">
            <a href="#"
              ><img
                class="logo"
                src="../assets/img/avada-drivers-logo-1x.png"
                alt="Avada logo"
            /></a>
          </div>
          <div class="col-lg-6">
            <ul class="d-flex flex-lg-row justify-content-between align-middle">
              <li
                v-for="(link, index) in Links"
                class="list-unstyled text-uppercase"
                :key="index"
              >
                <a href="#"
                  >{{ link }}
                  <span v-if="index == 3">{{ lable }}</span>
                </a>
              </li>
            </ul>
          </div>
          <div class="text-right col-lg-2 CTA">
            <button type="call" class="d-lg-block text-uppercase">
              {{ BtnTop }}
            </button>
          </div>
        </div>
      </div>
    </header>

    <!-- HERO -->

    <section class="hero">
      <div class="container-sm">
        <div class="row">
          <div class="col-lg-12">
            <h1>Drive with Avada</h1>
            <h2>We offer the finest driving tuition money can buy</h2>
          </div>
        </div>
      </div>
    </section>
  </section>
</template>

<script>
export default {
  name: "HeaderComponent",
  components: {},
  data() {
    return {
      Links: ["home", "about", "prices", "courses", "locations", "blog"],
      BtnTop: "book now",
      lable: "new",
    };
  },
};
</script>

<style lang="scss">
@import "../styles/general.scss";

/* CONTACTS */
.contacts {
  background-color: $gray-dark;
  height: 4em;
  color: $gray-light;
  font-size: 0.8em;
  span {
    line-height: 3em;
    font-weight: 100;
  }
}

header {
  background-color: $gray-transp;
  position: sticky;
  width: 100%;
  left: 0;
  top: 0;
  z-index: 2;

  &.active {
    background-color: $gray-dark;
  }

  .logo {
    max-width: 250px;
  }

  .row {
    height: 115px;
    &.active {
      height: 65px;
      background-color: $gray-dark;
    }
  }

  .hamburger {
    cursor: pointer;
    display: flex;
    justify-content: flex-end;

    div:hover > span {
      border-color: $green-main;
      transition: all 0.3s ease;
    }
    span {
      display: block;
      width: 30px;
      padding-bottom: 6px;
      border-bottom: 1px solid $white;

      &:first-of-type {
        border-bottom: 3px solid $white;
      }
      &:nth-of-type(2) {
        border-bottom: 2px solid $white;
      }
    }
  }

  ul {
    margin: 0;
    display: flex;
    align-items: center;
    flex-direction: column;
    height: 50%;

    li {
      line-height: 44px;
      cursor: pointer;
      position: relative;

      &::after {
        content: "";
        display: block;
        position: absolute;
        opacity: 0;
        left: 50%;
        transform: translate(-50%, 0);
        bottom: 0;
        width: 0;
        height: 2px;
        background-color: $green-main;
        transition: all 0.3s ease-in-out;
      }

      &:hover::after {
        content: "";
        opacity: 1;
        bottom: 0;
        width: 100%;
      }

      span {
        font-size: 9px;
        background-color: $green-main;
        padding: 5px 6px;
        border-radius: 4px;
        margin-left: 7px;
        font-weight: 800;
        line-height: 10px;
      }
    }
  }

  & .CTA a,
  & .CTA button {
    background-color: $green-main;
    padding: 10px 20px;
    width: 200px;
    border-radius: 22px;
    border: 2px solid transparent;
    text-align: center;
    width: 150px;
    display: block;
  }

  & .CTA a:hover,
  & .CTA button:hover {
    background-color: $green-sec;
    border: 2px solid $green-main;
  }

  & a,
  & button {
    color: $white;
    font-weight: 500;
    text-decoration: none;
    transition: all 0.3s ease-in-out;
  }

  & a:hover {
    text-decoration: none;
    color: $green-main;
  }

  & a:hover span {
    color: $white;
  }
}

/* HERO */
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

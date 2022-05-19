<template>
  <section>
    <!-- CONTACTS -->
    <section class="contacts">
      <div class="container">
        <div class="row">
          <div class="col-6">
            <span>We have a 95% Successful Pass Rate!</span>
          </div>
          <div class="col-6 text-end">
            <span>
              <i class="fa-solid fa-phone fa-rotate-270 px-2"></i>
              Give us a call to book your tuition! 1-800-555-555
            </span>
          </div>
        </div>
      </div>
    </section>

    <!-- HEADER -->
    <header>
      <div class="container">
        <div class="row align-items-center">
          <div class="col-4">
            <a href="#"
              ><img
                class="logo"
                src="../assets/img/avada-drivers-logo-1x.png"
                alt="Avada logo"
            /></a>
          </div>
          <div class="col-6">
            <ul class="d-flex flex-row justify-content-between align-middle">
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
          <div class="text-right col-2 CTA">
            <button type="call" class="d-block text-uppercase">
              {{ BtnTop }}
            </button>
          </div>
        </div>
      </div>
    </header>


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

<style lang="scss" scoped>
@import "../styles/general.scss";

.contacts {
  background-color: $gray-dark;
  height: 3em;
  color: $gray-light;
  font-size: 0.8em;
  span {
    line-height: 3em;
    font-weight: 100;
  }
}

header {
  background-color: $gray-transp;
  position: relative;
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

</style>

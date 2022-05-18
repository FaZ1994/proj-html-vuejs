<template>
  <section class="our-stats">
    <!-- our-stats -->
    <div class="container">
      <div class="row no-gutters">
        <div class="col-4">
          <div class="card-container">
            <div class="card text-center">
              <div class="ring-per-container">
                <div id="ring-per-pass">
                  <h1>95%</h1>
                </div>
              </div>
              <span>Pass Rate</span>
            </div>
          </div>
        </div>
        <div class="col-4">
          <div class="card-container">
            <div class="card text-center">
              <div class="ring-per-container">
                <div id="ring-per-rate">
                  <h1>100%</h1>
                </div>
              </div>
              <span>Referral Rate</span>
            </div>
          </div>
        </div>
        <div class="col-4">
          <div class="card-container">
            <div class="card text-center">
              <div class="ring-per-container">
                <div id="ring-per-accident">
                  <h1>0%</h1>
                </div>
              </div>
              <span>Accident Rate</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "OurStats",
  components: {},
  data() {
    return {};
  },
};
</script>

<style lang="scss">
@import "../styles/general.scss";

.our-stats {
  padding-bottom: 50px;
  border: none;
  position: relative;
  top: -60px;

  .card-container {
    background-color: $green-main;
    border-radius: 12px;
    box-shadow: $gray-transp 0px 25px 20px 0px;
    margin: 0 7px;
  }

  .ring-per-container {
    position: relative;
    height: 220px;
    margin: 50px 0;
  }

  .card {
    background-color: $white;
    border-radius: 5px 5px 12px 12px;
    height: 100%;
    border: none;
    position: relative;
    top: 6px;
  }

  & > div > div > div:nth-child(2) > div {
    margin: 50px 0;
  }

  .card span {
    display: block;
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
    font-size:1.2em;
    font-weight: 400;
    color: $gray-dark;
    text-transform: uppercase;
  }

}
</style>

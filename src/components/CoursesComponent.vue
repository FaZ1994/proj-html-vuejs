<template>
  <section>
    <section class="courses-sect">
      <div class="container">
        <div class="row text-center">
          <div class="col-5">
            <div class="courses-main">
              <h2>Courses</h2>
              <p>
                Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nunc
                ultrices auctor sapien id cursus. Aliquam maximus turpis in
                vehicula semper.
              </p>
              <button class="btn-green">Course information</button>
            </div>
          </div>
          <div class="col-7">
            <div class="row courses-others">
              <div class="col-4">
                <div>
                  <img
                    src="../assets/img/courses-passplus.jpg"
                    alt="courses-passplus"
                  />
                </div>
                <h4>Pass Plus</h4>
                <button class="btn-blue">Learn More</button>
              </div>
              <div class="col-4">
                <div>
                  <img
                    src="../assets/img/course-intensive.jpg"
                    alt="course-intensive"
                  />
                </div>
                <h4>Intensive Course</h4>
                <button class="btn-blue">Learn More</button>
              </div>
              <div class="col-4">
                <div>
                  <img
                    src="../assets/img/courses-instructor.jpg"
                    alt="courses-instructor"
                  />
                </div>
                <h4>Instructors</h4>
                <button class="btn-blue">Learn More</button>
              </div>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section class="triangular-base"></section>
  </section>
</template>

<script>
export default {
  name: "CoursesComponent",
  components: {},
  data() {
    return {};
  },
};
</script>

<style lang="scss" scoped>
@import "../styles/general.scss";

.courses-sect {
  background-image: url("../assets/img/promise-background.jpg");
  background-position: bottom;
  background-size: cover;
  padding: 80px 0;

  .courses-main {
    box-shadow: $gray-transp 0px 25px 20px 0px;
    padding: 50px 30px;
    margin: 0 10px 30px;
    border-radius: 10px;
    background-color: $white;
    position: relative;
    top: -110px;
    overflow: hidden;

    &::after {
      content: "new";
      position: absolute;
      display: block;
      width: 120px;
      height: 70px;
      line-height: 100px;
      left: -42px;
      top: -18px;
      background: $green-main;
      text-transform: uppercase;
      color: $white;
      font-weight: 700;
      transform: rotateZ(-45deg);
    }

    h2 {
      font-size: 40px;
      color: $gray-dark;
      margin-bottom: 50px;
      font-weight: 700;
    }

    p {
      font-size: 16px;
      color: $gray-transp;
      line-height: 2;
      margin-bottom: 50px;
    }
  }

  img {
    max-width: 100%;
    transition: all 1s ease-in-out;
  }

  .courses-others {
    img:hover {
      transform: scale(1.15);
    }

    & > div {
      padding: 15px;
      color: $blue-main;
    }

    & > div > div {
      overflow: hidden;
    }

    h4 {
      margin: 15px 0;
    }
  }

  .row.courses-others div div {
    max-width: 450px;
    margin: auto;
  }
}

.triangular-base {
  background-color: #e4e9ed;
  clip-path: polygon(0% 0%, 100% 0%, 50% 100%);
  height: 120px;
  position: relative;
  top: -1px;
}
</style>

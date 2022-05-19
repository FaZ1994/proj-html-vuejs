<template>
  <section class="latest_news">
    <div class="container">
      <div class="row background">
        <div class="col-12">
          <div class="row foreground">
            <div class="col-12">
              <h2 class="text-center">Latest News</h2>
            </div>
            <div class="col-12">
              <div class="row cards-section align-items-center">
                <div class="col-6">
                  <div class="blog-news text-center">
                    <div class="img-box">
                      <a href="#"
                        ><img
                          src="../assets/img/blog-choosecar-700x441.jpg"
                          alt="blog-choosecar"
                      /></a>
                    </div>
                    <a href="#">What Car to Start With?</a>
                    <p>
                      February 7th, 2019

                      <a href="#">0 Comments</a>
                    </p>
                    <p>Lorem ipsum dolor sit amet, consectetur adipiscing</p>
                  </div>
                </div>
                <div class="col-6">
                  <div class="blog-news text-center">
                    <div class="img-box">
                      <a href="#"
                        ><img
                          src="../assets/img/blogpost-10and2-700x441.jpg"
                          alt="blogpost"
                      /></a>
                    </div>
                    <a href="#">Avada Driving School Expanding</a>
                    <p>
                      February 7th, 2019

                      <a href="#">0 Comments</a>
                    </p>
                    <p>Lorem ipsum dolor sit amet, consectetur adipiscing</p>
                  </div>
                </div>
              </div>
            </div>
            <div class="col-12 text-center cta-section">
              <button class="btn-green">More from the blog</button>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="container">
      <div class="row">
        <div class="col-12">
          <div class="row triangular-element">
            <div class="col-12"></div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "LatestNewsComponent",
  components: {},
};
</script>

<style lang="scss" scoped>
@import "../styles/general.scss";

.latest_news {
  background-image: url("../assets/img/latestnews-background.jpg");
  background-size: cover;
  padding-bottom: 50px;

  & > div:first-of-type {
    border-radius: 5px 5px 0 0;
    box-shadow: $black-transp-04 0px 45px 40px 0px;
  }

  h2 {
    font-size: 40px;
    font-weight: 700;
    color: $gray-dark;
    margin: 50px 0;
  }

  a {
    font-size: 21px;
    margin: 15px 0;
    font-weight: 700;
    color: $green-main;
    text-decoration: none;

    &:hover {
      text-decoration: none;
    }
  }

  .blog-news p {
    &:first-of-type {
      font-size: 12px;
      font-weight: 400;
      color: $gray-transp;

      a {
        font-size: 12px;
        font-weight: 400;
      }
    }
    &:last-of-type {
      font-size: 16px;
      font-weight: 400;
      color: $gray-transp;
      line-height: 2;
    }
  }

  span {
    display: block;
    font-size: 12px;
    color: $gray-transp;
  }

  img {
    max-width: 100%;
    transition: all 0.5s ease-in-out;
    &:hover {
      transform: scale(1.1);
    }
  }

  .img-box {
    margin-bottom: 15px;
    overflow: hidden;
  }

  .cards-section {
    & > div:first-of-type .blog-news {
      padding: 0 40px;
    }

    & > div:last-of-type .blog-news {
      padding: 40px;
    }
  }

  .cta-section {
    padding: 40px 0;
  }

  .triangular-element {
    height: 100px;
    background-color: $white;
    clip-path: polygon(0% 0%, 0% 5%, 50% 100%, 100% 5%, 100% 0%);
    position: relative;
    top: -5px;
  }

  .background {
    background-color: $blue-main;
    border-radius: 10px 10px 0 0;
    margin-top: -50px;
    position: relative;
  }
  .foreground {
    margin-top: -25px;
    background-color: $white;
    border-radius: 5px 5px 0 0;
  }
}
</style>

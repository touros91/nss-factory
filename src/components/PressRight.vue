<template>
  <div
    data-aos="zoom-in"
    data-aos-delay="300"
    data-aos-once="true"
    class="col-xs-12 col-lg-6 right d-none d-xxl-block"
  >
    <div class="row">
      <div class="col-xs-12 col-lg-6 left">
        <div class="image">
          <div
            id="demo"
            class="carousel slide d-none d-lg-block"
            data-bs-ride="carousel"
          >
            <div class="carousel-inner">
              <div class="carousel-item active">
                <img
                  :src="require(`@/assets/img/watch.png`)"
                  class="d-block w-100"
                  alt="Handmade Watch Laboratory"
                />
              </div>
              <div class="carousel-item">
                <img
                  :src="require(`@/assets/img/watch-lab.jpeg`)"
                  class="d-block w-100"
                  alt="Handmade Watch Laboratory"
                />
              </div>
              <div class="carousel-item">
                <img
                  :src="require(`@/assets/img/watch3.webp`)"
                  class="d-block w-100"
                  alt="Henry London Watch"
                />
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="col-xs-12 col-lg-6 press">
        <h6>PRESS</h6>
        <p class="date">18 SETTEMBRE 2015</p>
        <h3>Most Important Days on Watchlab</h3>
        <div class="icons">
          <font-awesome-icon
            class="arrow-left"
            icon="fa-solid fa-angle-left"
            data-bs-target="#demo"
            data-bs-slide="prev"
          />
          <font-awesome-icon
            class="arrow-right"
            icon="fa-solid fa-angle-right"
            data-bs-target="#demo"
            data-bs-slide="next"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@import "src/assets/style/partials/variables.scss";
@import "src/assets/style/partials/mixins.scss";

.left {
  position: relative;
  .image {
    position: absolute;
    top: 30%;
    left: -80%;

    img {
      width: 100%;
    }
  }
}
.right {
  width: 50%;
  background: #f8f8f8;
  position: relative;

  .col-6 {
    border: 1px solid;
  }

  .col-lg-6.press {
    @include flex(column, center, center);
    height: 910px;
    text-align: center;

    h6 {
      margin-right: auto;
      margin-bottom: 0px;
      font-family: $montserrat-bold;
    }

    h3 {
      font-family: $miller-display;
      text-align: left;
    }

    .date {
      color: #d5cec0;
      margin-right: auto;
      margin-bottom: 50px;
      font-family: $montserrat-bold;
    }
  }

  .icons {
    margin-right: auto;
    margin-top: 50px;

    .arrow-left,
    .arrow-right {
      cursor: pointer;
    }

    .arrow-right {
      margin-left: 50px;
    }
  }
}

.carousel {
  overflow: hidden;
  width: 500px;

  color: $color-white;
  .carousel-item {
    img {
      height: 500px;
      object-fit: cover;
    }
  }

  .carousel-inner::after {
    content: "";
    position: absolute;
    left: 0;
    width: 100%;
    height: 100%;
    z-index: 1;
    background-color: rgba(0, 0, 0, 0.4);
    transition: all 0.5s;
  }
  &:hover .carousel-inner::after {
    background-color: rgba(0, 0, 0, 0.1);
  }
}
</style>
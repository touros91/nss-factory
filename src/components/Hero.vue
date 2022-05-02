<template>
  <div class="hero">
    <div class="content">
      <h6>LONDON COLLECTION SEASON</h6>
      <h1>
        New Selection Of <br />
        Herny London
      </h1>
      <p>An estimable experience in the modern collection house</p>
      <button>Discover</button>
    </div>
    <!-- slider -->
    <div
      id="carouselExampleControls"
      class="carousel slide d-none d-lg-block"
      data-bs-ride="carousel"
    >
      <div class="carousel-inner">
        <div class="carousel-item active">
          <img
            :src="require(`@/assets/img/carousel1.webp`)"
            class="d-block w-100"
            alt="Woman Henry London Watch"
          />
        </div>
        <div class="carousel-item">
          <img
            :src="require(`@/assets/img/carousel2.jpeg`)"
            class="d-block w-100"
            alt="Man Henry London Watch"
          />
        </div>
        <div class="carousel-item">
          <img
            :src="require(`@/assets/img/carousel3.webp`)"
            class="d-block w-100"
            alt="Women Henry London Watch"
          />
        </div>
      </div>
      <div class="carousel-text">
        The Path to Success <br />
        with Watchlab
      </div>
      <button
        class="carousel-control-next"
        type="button"
        data-bs-target="#carouselExampleControls"
        data-bs-slide="next"
      >
        <span class="">NEXT</span>
        <font-awesome-icon icon="fas fa-angle-right" class="animation" />
      </button>
    </div>
    <!-- /slider -->
  </div>
</template>

<style lang="scss" scoped>
@import "src/assets/style/partials/variables.scss";
@import "src/assets/style/partials/mixins.scss";

.hero {
  width: 100vw;
  height: 650px;
  padding: 400px 0;
  position: relative;
  background-image: url("../assets/img/office.jpg");
  object-fit: cover;
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
  box-shadow: inset 0 0 0 1000px rgba(0, 0, 0, 0.4);
  @include flex-row(center, center);

  .content {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    color: $color-white;
    font-weight: 900;
    text-align: center;
    font-family: $montserrat-bold;

    h6 {
      font-size: 14px;
    }

    h1 {
      font-family: $miller-display;
      font-size: $main-title;
    }

    p {
      font-size: 12px;
      font-family: $montserrat;
    }

    button {
      padding: 8px 70px;
      border: 1px solid $color-white;
      color: $color-white;
      font-weight: 100px;
      background: transparent;
      cursor: pointer;
      font-family: $miller-display;

      &:hover {
        background: $color-beige;
      }
    }
  }
}

.carousel {
  color: $color-white;
  overflow: hidden;
  width: 350px;
  position: absolute;
  bottom: 0;
  right: 50px;

  .carousel-item {
    img {
      height: 230px;
      object-fit: cover;
    }
  }
  .carousel-control-next {
    opacity: 1;
    top: 65%;
    right: 50px;
    font-family: $montserrat-bold;

    .fa-angle-right {
      margin-left: 20px;
    }
  }
  .carousel-text {
    position: absolute;
    z-index: 1;
    font-family: $miller-display;
    top: 30px;
    left: 20px;
    font-size: 23px;
  }
  .carousel-inner::after {
    content: "";
    width: 100%;
    height: 100%;
    position: absolute;
    left: 0;
    z-index: 1;
    background-color: rgba(0, 0, 0, 0.2);
    transition: all 0.5s;
  }
}

.carousel:hover .animation {
  animation: move 1s infinite;
}
@keyframes move {
  from {
    transform: translateX(0);
    opacity: 0;
  }
  to {
    transform: translateX(15px);
    opacity: 1;
  }
}
</style>
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
    <div class="slider d-none d-lg-block">
      <div class="slider-img">
        <img
          src="https://www.holzkern.com/media/holzkern/cache/1080/catalog/product/b/e/belvue1.2.webp"
          alt="Watch"
        />
        <p class="p">The Path to Success with Watchlab</p>
        <button>
          NEXT
          <font-awesome-icon class="arrow" icon="fa-solid fa-angle-right" />
        </button>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.hero {
  width: 100vw;
  height: 650px;
  position: relative;
  background-image: url(../assets/img/office.jpeg);
  object-fit: cover;
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
  box-shadow: inset 0 0 0 1000px rgba(0, 0, 0, 0.4);
  display: flex;
  justify-content: center;
  align-items: center;

  .content {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    color: white;
    font-weight: 900;
    text-align: center;
    font-family: "Montserrat-Bold";

    h6 {
      font-size: 14px;
    }

    h1 {
      font-family: "Miller-Display";
      font-size: 70px;
    }

    p {
      font-size: 12px;
      font-family: "Montserrat-Regular";
    }

    button {
      padding: 8px 70px;
      border: 1px solid white;
      color: white;
      font-weight: 100px;
      background: transparent;
      cursor: pointer;
      font-family: "Miller-Display";

      &:hover {
        background: #d0c3b6;
      }
    }
  }

  .slider {
    width: 250px;
    position: absolute;
    right: 50px;
    top: 450px;
    // position: relative;

    .slider-img {
      position: relative;

      img {
        width: 100%;
        height: 200px;
        object-fit: cover;
        opacity: 0.9;
      }

      p {
        position: absolute;
        left: 15px;
        top: 25px;
        color: white;
        width: 200px;
        font-family: "Miller-Display";
        font-size: 20px;
      }

      button {
        position: absolute;
        right: 25px;
        bottom: 25px;
        border: none;
        background: transparent;
        color: white;
        font-family: "Montserrat-Regular";
        font-size: 15px;

        .arrow {
          margin-left: 15px;
        }
      }
    }
  }
}
</style>
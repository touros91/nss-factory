<template>
  <div>
    <div class="image">
      <img
        src="https://icdn.digitaltrends.com/image/digitaltrends/best-macbooks-air.jpg"
        alt="Man with Watch"
      />
      <div class="content">
        <h2>Get in Touch</h2>
        <p>
          DISCOVER MORE ABOUT NEWS, <br />
          EXCLUSIVE EVENTS AND DISCOUNT
        </p>
        <div class="input">
          <input class="text" type="text" placeholder="type your email" />
          <input class="submit" type="submit" value="ok" />
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@import "src/assets/style/partials/variables.scss";

div {
  color: $color-white;
  font-family: $miller-display;
  margin: 50px 25px 0 25px;

  .image {
    position: relative;
    height: 450px;

    &::after {
      content: "";
      position: absolute;
      left: 0;
      width: 100%;
      height: 100%;
      z-index: 1;
      background-color: rgba(0, 0, 0, 0.4);
    }

    img {
      width: 100%;
      height: 450px;
      opacity: 0.8;
      object-fit: cover;
    }
    .content {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      text-align: center;
      z-index: 2;

      h2 {
        font-size: $main-title;
      }

      p {
        font-size: 12px;
        font-family: $montserrat;
        padding: 0 30px;
      }
      .input {
        input {
          background: transparent;
          color: $color-white;
          border: 1px solid;
          outline: none;
          &::placeholder {
            color: $color-white;
          }
        }
        .text {
          padding: 10px 20px 10px 15px;
        }

        .submit {
          padding: 10px;
          margin-left: 10px;
          &.submit:hover {
            background: $color-beige;
          }
        }
      }
    }
  }
}

@media only screen and (min-width: 0px) and (max-width: 992px) {
  .content {
    margin: 0 auto;
    .submit {
      margin-top: 20px;
    }
  }
}
</style>
<template>
  <div class="col-xs-12 col-lg-6">
    <a href="#">
      <div class="image">
        <img
          src="https://images.unsplash.com/photo-1594938384824-022767a58e11?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxzZWFyY2h8M3x8ZWxlZ2FudCUyMG1hbnxlbnwwfDJ8MHx8&auto=format&fit=crop&w=800&q=60"
          alt="Man with Watch"
        />
        <div class="content">
          <h6>INSTAGRAM</h6>
          <h2>
            Discover <br />
            Watch Lab
          </h2>
        </div>
      </div>
    </a>
  </div>
</template>

<script>
export default {
  props: {
    source: {
      type: String,
    },
  },
};
</script>

<style lang="scss" scoped>
@import "src/assets/style/partials/variables.scss";

div {
  color: $color-white;
  font-family: $miller-display;

  .col-lg-6 {
    padding: 0;

    .image {
      position: relative;
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
        opacity: 0.8;
      }
      .content {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        text-align: center;
        z-index: 2;
        h6 {
          font-family: $montserrat-bold;
        }
        h2 {
          font-size: 50px;
        }
      }
    }
  }
}
</style>
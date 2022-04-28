<template>
  <div class="container-fluid">
    <div class="row">
      <div class="col-xs-12 col-lg-6">
        <h2>
          Press from <br />
          Watch Lab Studio
        </h2>
        <p>
          On the other hand, we denounce with righteous indignation and dislike
          men who are so beguiled and demoralized by the charms of pleasure of
          the moment, so blinded by desire, that they cannot foresee the pain
          trouble
        </p>
      </div>
      <div class="col-xs-12 col-lg-6 right">
        <div class="image">
          <img src="@/assets/img/watch.png" alt="Handmade watch" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.container-fluid {
  padding: 50px 0;

  .col-xs-12,
  .col-lg-6 {
    min-height: 670px;
    font-family: "Miller-Display";

    h2 {
      font-size: 50px;
    }

    p {
      color: #acacac;
      font-size: 15px;
      padding: 50px 250px 0 0;
    }

    &.right {
      width: 50%;
      background: #f8f8f8;
      position: relative;
    }

    .image {
      width: 600px;
      position: absolute;
      top: 130px;
      left: -250px;

      img {
        width: 100%;
      }
    }
  }
}
</style>
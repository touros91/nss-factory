<template>
  <div class="copyright d-flex justify-content-between">
    <div class="left">
      <small
        >Copyright Watch/Lab all rights reserved website by nssfactory</small
      >
    </div>
    <div class="right"><small>website by nssfactory</small></div>
  </div>
</template>

<style lang="scss" scoped>
@import "src/assets/style/partials/variables.scss";

.copyright {
  display: flex;
  background: #303030;
  font-size: 12px;

  padding: 50px 0;
  color: $color-beige;
  background: #303030;
  font-family: $merriweather;

  .left {
    padding: 0 100px;
  }
  .right {
    padding-right: 100px;
  }
}
@media only screen and (min-width: 0px) and (max-width: 992px) {
  .copyright {
    display: flex;
    flex-direction: column;

    .left {
      padding: 0 30px;
      margin-bottom: 30px;
    }

    .right {
      padding: 0 30px;
    }
  }
}
</style>
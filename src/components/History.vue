<template>
  <div>
    <div class="row">
      <div class="col">
        <h2>
          History and <br />
          Patriarcal season
        </h2>
      </div>
    </div>
    <div class="row">
      <div class="col-xs-12 col-lg-6 left">
        <p>
          On the other hand, we denounce with righteous indignation and dislike
          men who are so beguiled and demoralized by the charms of pleasure of
          the moment, so blinded by desire
        </p>
      </div>
      <div class="col-xs-12 col-lg-6">
        <p>
          But I must explain to you how all this mistaken idea of denouncing
          pleasure and praising pain was born and I will give you a complete
          account of the system, and expound the actual teachings of the great
          explorer of the truth, the master-builder of human happiness. No that
          are extremely painful
        </p>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@import "src/assets/style/partials/variables.scss";

div {
  font-family: $miller-display;
  padding: 20px 0;
  h2 {
    color: $color-title;
    margin-bottom: 20px;
    font-size: $main-title;
  }

  p {
    color: $color-paragraph;
    font-size: 15px;
    text-align: left;
    font-family: $merriweather;
  }

  .left {
    padding-right: 150px;
  }
}

@media only screen and (min-width: 0px) and (max-width: 992px) {
  div .left {
    padding-right: 0px;
  }
}
</style>
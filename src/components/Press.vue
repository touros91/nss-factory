<template>
  <div class="col-xs-12 col-xxl-6">
    <h2>
      Press from <br />
      Watch Lab Studio
    </h2>
    <p>
      On the other hand, we denounce with righteous indignation and dislike men
      who are so beguiled and demoralized by the charms of pleasure of the
      moment, so blinded by desire, that they cannot foresee the pain trouble
    </p>
  </div>
</template>

<style lang="scss" scoped>
@import "src/assets/style/partials/variables.scss";

.col-xs-12 {
  font-family: $miller-display;
  color: #212529;

  h2 {
    text-align: left;
    padding-bottom: 50px;
    font-size: $main-title;
  }
}

p {
  color: $color-paragraph;
  font-size: 15px;
  text-align: left;
  font-family: $merriweather;
  padding-right: 350px;
}

@media (max-width: 992px) {
  p {
    padding-right: 0;
  }
}
</style>
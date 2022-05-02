<template>
  <div class="col-xs-12 col-lg-6">
    <h6>LONDON COLLECTION SEASON</h6>
    <h3>{{ title }}</h3>
    <p>
      On the other hand, we denounce with righteous indignation and dislike men
      who are so beguiled and demoralized by the charms of pleasure of the
      moment, so blinded by desire
    </p>
    <button>Discover</button>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
    },
  },
};
</script>

<style lang="scss" scoped>
@import "src/assets/style/partials/variables.scss";
@import "src/assets/style/partials/mixins.scss";

div {
  padding: 30px;
  font-family: $miller-display;
  @include flex(column, center, center);

  .col-xs-12 {
    text-align: center;
  }

  .col-6 {
    @include flex(column, center, center);
  }

  h3 {
    padding: 20px 0;
    color: $color-title;
    font-size: 34px;
    width: 50%;
    display: flex;
    justify-content: center;
  }

  h6 {
    color: $color-title;
    font-size: 10px;
    font-family: $montserrat-bold;
  }

  p {
    text-align: center;
    color: $color-paragraph;
    font-size: 15px;
    font-family: $merriweather;
  }

  button {
    padding: 8px 70px;
    border: 1px solid $color-beige;
    color: $color-beige;
    font-weight: 100px;
    background: transparent;
    cursor: pointer;
    font-family: $miller-display;
    margin: 40px 0;

    &:hover {
      background: $color-beige;
      color: $color-white;
    }
  }
}
</style>
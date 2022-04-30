<template>
  <div class="col-xs-12 col-lg-6 mt-5 mt-lg-0">
    <img :src="require(`@/${source}`)" alt="London Bus" />
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
  .col-lg-6 {
    padding: 0;
    img {
      width: 100%;
    }
  }
}
</style>
<template>
  <div
    data-aos="zoom-in"
    data-aos-delay="300"
    class="col-xs-12 col-lg-6 mb-5 mb-lg-0"
  >
    <img :src="require(`@/${source}`)" alt="Store" />
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
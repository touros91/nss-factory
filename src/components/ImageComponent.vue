<template>
  <div class="col-xs-12 col-lg-6">
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
div {
  padding-right: var(--bs-gutter-x, 1.75rem);
  padding-left: var(--bs-gutter-x, 1.75rem);

  .col-xs-12 {
    width: 100%;
    img {
      width: 100%;
    }
  }
  .col-lg-6 {
    width: 50%;
    padding: 0;
    img {
      width: 100%;
    }
  }
}
</style>
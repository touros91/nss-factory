<template>
  <div class="col-xs-12 col-lg-6">
    <h6>LONDON COLLECTION SEASON</h6>
    <h3>{{ title }}</h3>
    <p>
      On the other hand, we denounce with righteous indignation and dislike men
      who are so beguiled and demoralized by the charms of pleasure of the
      moment, so blinded by desire
    </p>
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
div {
  padding: 30px;
  font-family: "Miller-Display";
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;

  .col-xs-12 {
    text-align: center;
  }

  .col-6 {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }

  h3 {
    padding: 20px 0;
    color: #111111;
    font-size: 34px;
    width: 50%;
  }

  h6 {
    color: #111111;
    font-size: 10px;
    font-family: "Montserrat-Bold";
  }

  p {
    text-align: center;
    color: #acacac;
    font-size: 15px;
    width: 60%;
  }
}
</style>
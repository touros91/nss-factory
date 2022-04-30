<template>
  <div class="container footer">
    <div class="row">
      <div class="col-xs-12 col-md-4 left d-flex flex-column">
        <h3 class="logo">WATCH/LAB</h3>
        <p>
          Watch/Lab
          <span class="innovation">Innovation brings success</span>
        </p>
        <p>Via Borgona 5, Milan</p>
        <p>Italy</p>
      </div>
      <div class="col-xs-12 col-md-8 right">
        <div class="row">
          <div class="col">
            <ul>
              <li v-for="(item, index) in footerData[0]" :key="index">
                <a href="#">{{ item }}</a>
              </li>
            </ul>
          </div>
          <div class="col">
            <ul>
              <li v-for="(item, index) in footerData[1]" :key="index">
                <a href="#">{{ item }}</a>
              </li>
            </ul>
          </div>
          <div class="col">
            <ul class="last-list">
              <li v-for="(item, index) in footerData[2]" :key="index">
                <a href="#">{{ item }}</a>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    footerData: {
      type: Array,
    },
  },
};
</script>

<style lang="scss" scoped>
@import "src/assets/style/partials/variables.scss";

.footer {
  padding: 50px 20px;
  min-height: 400px;
  background: #333333;
  color: $color-beige;
  font-family: "Merriweather-Regular";
  font-size: 14px;

  .left {
    .logo {
      color: white;
      max-width: 250px;
      font-weight: 700;
      font-size: 25px;
      letter-spacing: 3px;
      text-decoration: none;
      font-family: $montserrat-bold;
      margin-bottom: 40px;
    }

    .innovation {
      margin-left: 30px;
    }
  }

  .right {
    padding: 60px 0;

    ul {
      width: 250px;
      display: flex;
      flex-direction: column;
      list-style: none;

      li {
        margin: 10px 0;

        a {
          text-decoration: none;
          color: $color-beige;
        }
      }
    }

    .last-list li:nth-child(3) {
      font-family: $montserrat-bold;
      letter-spacing: 3px;
    }
    .last-list li:last-child {
      font-family: $montserrat-bold;
      letter-spacing: 3px;
    }
  }
}
</style>
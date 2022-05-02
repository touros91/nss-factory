<template>
  <div class="contenitore">
    <div class="title">
      <h3 class="logo">WATCH/LAB</h3>
    </div>

    <div class="body">
      <div class="mid-one">
        <div class="one">
          <p>
            Watch/Lab
            <span class="innovation">Innovation brings success</span>
          </p>
          <p>Via Borgona 5, Milan</p>
          <p>Italy</p>
        </div>
      </div>

      <div class="mid-two">
        <div class="two">
          <ul>
            <li v-for="(item, index) in footerData[0]" :key="index">
              <a href="#">{{ item }}</a>
            </li>
          </ul>
        </div>
        <div class="three">
          <ul>
            <li v-for="(item, index) in footerData[1]" :key="index">
              <a href="#">{{ item }}</a>
            </li>
          </ul>
        </div>
        <div class="four">
          <ul class="last-list mb-0">
            <li v-for="(item, index) in footerData[2]" :key="index">
              <a href="#">{{ item }}</a>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
  <!-- <div>
    <div class="left">
      <h3 class="logo">WATCH/LAB</h3>
      <p>
        Watch/Lab
        <span class="innovation">Innovation brings success</span>
      </p>
      <p>Via Borgona 5, Milan</p>
      <p>Italy</p>
    </div>
    <div class="right">
      <div class="container-fluid">
        <div class="row">
          <div class="col-4">
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
          <div class="col mt-5 mt-lg-0">
            <ul class="last-list mb-0">
              <li v-for="(item, index) in footerData[2]" :key="index">
                <a href="#">{{ item }}</a>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </div> -->
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

.title {
  padding: 100px 0 0 100px;
  .logo {
    color: $color-white;
    max-width: 250px;
    font-weight: 700;
    font-size: 25px;
    letter-spacing: 3px;
    text-decoration: none;
    font-family: $montserrat-bold;
    margin-bottom: 35px;
  }
}
.body {
  color: $color-beige;
  display: flex;
  font-family: $merriweather;
  font-size: 12px;
  padding-bottom: 50px 0;

  ul {
    padding-left: 0px;
    color: $color-beige;

    li {
      list-style: none;
      color: $color-beige;
      margin-bottom: 20px;

      a {
        color: $color-beige;
        text-decoration: none;
      }
    }
  }
  .mid-one {
    padding-left: 100px;
    .innovation {
      margin-left: 20px;
    }
  }
  .mid-two {
    display: flex;
    margin-left: 200px;
    padding-bottom: 100px;
    width: 500px;
    justify-content: space-around;
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

// media query
@media only screen and (min-width: 993px) and (max-width: 1400px) {
  // .title {
  //   padding: 100px 0 50px 100px;
  // }
  .mid-one {
    .two {
      ul {
        padding: 0;
      }
    }
  }

  body {
    .mid-two {
      flex-direction: column;
      margin-left: 0px;
      width: auto;
    }
  }
}

@media only screen and (min-width: 0px) and (max-width: 992px) {
  .title {
    padding: 0;
    display: flex;
    justify-content: center;
    padding-top: 50px;
    text-align: center;
  }

  .body {
    .mid-one {
      padding: 30px;
      text-align: center;

      .two {
        ul {
          padding: 0;
        }
      }
    }
  }

  .body {
    display: flex;
    flex-direction: column;
    .title {
      padding: 100px 0 50px 100px;
    }
    .mid-two {
      display: flex;
      flex-direction: column;
      text-align: center;
      margin-left: 0px;
      padding: 30px;
      width: auto;
    }
  }
}
</style>
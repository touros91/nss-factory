<template>
  <div id="app">
    <!-- header with navigation bar  -->
    <header>
      <NavBar :navBar="navBar" />
    </header>
    <!-- main section  -->
    <main>
      <!-- Hero with carousel  -->
      <section>
        <Hero />
      </section>
      <div class="main-container">
        <section class="container-fluid">
          <div class="row row-padding">
            <History />
          </div>
        </section>
        <!-- Temporary Store and New Collection section  -->
        <section class="container-fluid">
          <div class="row row-padding">
            <Collection title="Temporary Store" />
            <ImageComponent source="assets/img/store-snow.png" />
          </div>
          <div class="row row-padding">
            <ImageComponent source="assets/img/store.png" />
            <Collection title="New Collection Henry London" />
          </div>
        </section>
        <!-- Press with carousel section  -->
        <section class="container-fluid mt-5">
          <div class="row row-padding">
            <Press />
            <PressRight />
          </div>
        </section>
        <!-- Instagram and images section  -->
        <section class="container-fluid mt-5">
          <div class="row row-padding">
            <Elegant source="assets/img/man.jpeg" />
            <div
              class="col-xs-12 col-lg-6"
              data-aos="flip-right"
              data-aos-easing="ease-out-cubic"
              data-aos-duration="2000"
              data-aos-delay="300"
              data-aos-once="true"
            >
              <div class="row">
                <ImageSmall source="assets/img/bus.png" />
                <ImageSmall source="assets/img/two-watches.png" />
              </div>
              <div class="row">
                <ImageSmall source="assets/img/dark-watch.png" />
                <ImageSmall source="assets/img/light-watch.png" />
              </div>
            </div>
          </div>
        </section>
        <!-- Newsletter section  -->
        <section>
          <GetInTouch />
        </section>
      </div>
      <!-- History section  -->
    </main>
    <!-- footer  -->

    <footer>
      <div class="main-container row-padding">
        <Footer :footerData="footerData" class="footer-bg" />
        <Copyright />
      </div>
    </footer>
  </div>
</template>

<script>
import NavBar from "./components/NavBar";
import Hero from "./components/Hero";
import History from "./components/History";
import Collection from "./components/Collection";
import ImageComponent from "./components/ImageComponent";
import Press from "./components/Press";
import PressRight from "./components/PressRight";
import Elegant from "./components/Elegant";
import ImageSmall from "./components/ImageSmall";
import GetInTouch from "./components/GetInTouch";
import Footer from "./components/Footer";
import Copyright from "./components/Copyright";

export default {
  name: "App",
  components: {
    NavBar,
    Hero,
    History,
    Collection,
    ImageComponent,
    Press,
    PressRight,
    Elegant,
    ImageSmall,
    GetInTouch,
    Footer,
    Copyright,
  },
  data() {
    return {
      navBar: [
        "About us",
        "Brand",
        "Projects",
        "Magazine",
        "Press",
        "Contacts",
      ],
      footerData: [
        ["About us", "Brand", "Projects", "Magazine"],
        ["Press", "Contacts", "Privacy Policy", "Search"],
        ["T.+39 392 9133937", "M.info@watch-lab-it", "FACEBOOK", "INSTAGRAM"],
      ],
    };
  },
};
</script>

<style lang="scss">
@import "src/assets/style/common.scss";
@import "src/assets/style/partials/variables.scss";
@import "src/assets/style/partials/mixins.scss";

@font-face {
  font-family: $montserrat;
  src: local("Montserrat"),
    url(./assets/font/Montserrat-Regular.ttf) format("truetype");
}
@font-face {
  font-family: $montserrat-bold;
  src: local("Montserrat"),
    url(./assets/font/Montserrat-Bold.ttf) format("truetype");
}
@font-face {
  font-family: $miller-display;
  src: local("Miller"),
    url(./assets/font/Miller-Display_30501.ttf) format("truetype");
}
@font-face {
  font-family: $merriweather;
  src: local("Merriweathert"),
    url(./assets/font/Merriweather-Regular.ttf) format("truetype");
}

.main-container {
  width: 85%;
  margin: auto;
}
.row-padding {
  padding: 0 50px;
}

.footer-bg {
  background: #333333;
}
</style>

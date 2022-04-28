<template>
  <div id="app">
    <header>
      <NavBar :navBar="navBar" />
    </header>
    <main>
      <section>
        <Hero />
      </section>
      <section class="container-fluid">
        <div class="row">
          <History />
        </div>
      </section>
      <section class="container-fluid">
        <div class="row">
          <Collection title="Temporary Store" />
          <ImageComponent source="assets/img/store-snow.png" />
        </div>
        <div class="row">
          <ImageComponent source="assets/img/store.png" />
          <Collection title="New Collection Henry London" />
        </div>
      </section>
      <section>
        <Press />
      </section>
    </main>
  </div>
</template>

<script>
import NavBar from "./components/NavBar";
import Hero from "./components/Hero";
import History from "./components/History";
import Collection from "./components/Collection";
import ImageComponent from "./components/ImageComponent";
import Press from "./components/Press";

export default {
  name: "App",
  components: {
    NavBar,
    Hero,
    History,
    Collection,
    ImageComponent,
    Press,
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
    };
  },
};
</script>

<style lang="scss">
@import "src/assets/style/common.scss";
@font-face {
  font-family: "Montserrat-Regular";
  src: local("Montserrat"),
    url(./assets/font/Montserrat-Regular.ttf) format("truetype");
}
@font-face {
  font-family: "Montserrat-Bold";
  src: local("Montserrat"),
    url(./assets/font/Montserrat-Bold.ttf) format("truetype");
}
@font-face {
  font-family: "Miller-Display";
  src: local("Miller"),
    url(./assets/font/Miller-Display_30501.ttf) format("truetype");
}
@font-face {
  font-family: "Merriweather-Regular";
  src: local("MontsMerriweathererrat"),
    url(./assets/font/Merriweather-Regular.ttf) format("truetype");
}

.row {
  padding: 0 50px;
}
</style>

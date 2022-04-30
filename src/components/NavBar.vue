<template>
  <nav class="navbar navbar-expand-lg navbar-light">
    <div class="container-fluid">
      <a href="#" class="logo">WATCH/LAB</a>
      <button
        class="navbar-toggler"
        type="button"
        data-bs-toggle="collapse"
        data-bs-target="#navbarSupportedContent"
        aria-controls="navbarSupportedContent"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul class="navbar-nav me-auto mb-2 mb-lg-0">
          <li class="nav-item" v-for="(item, index) in navBar" :key="index">
            <a class="nav-link active" aria-current="page" href="#">{{
              item
            }}</a>
          </li>
        </ul>
        <form class="d-flex justify-content-center">
          <input class="input-search" type="text" />
          <font-awesome-icon icon="fa-solid fa-magnifying-glass" />
        </form>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  props: {
    navBar: {
      type: Array,
    },
  },
};
</script>

<style lang="scss" scoped>
@import "src/assets/style/partials/variables.scss";

.navbar-light .navbar-nav .nav-link.active:hover {
  border-bottom: 1px solid;
  color: $color-beige;
}

.me-auto {
  margin-left: 50px;
}

.navbar-collapse {
  margin-right: 50px;
}

nav {
  top: 0px;
  width: 100%;
  font-family: "Montserrat";
}

.navbar {
  padding-top: 0px;
  padding-bottom: 0px;
  font-family: "Montserrat";
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  z-index: 3;

  .container-fluid {
    padding-left: 0px;
    background: $color-white;

    ul {
      margin-bottom: 0;
      width: 100%;
      padding-left: 0;
      display: flex;
      justify-content: space-evenly;

      li {
        list-style: none;
        font-weight: 600;
        cursor: pointer;

        &:hover {
          color: #333333;
        }

        a {
          text-decoration: none;
          text-align: center;
        }

        a:hover {
          color: #333333;
        }
      }
    }

    .logo {
      background-color: #d0c4b6;
      color: $color-white;
      max-width: 250px;
      font-weight: 700;
      font-size: 25px;
      padding: 24px;
      letter-spacing: 3px;
      text-decoration: none;
      font-family: $montserrat-bold;
    }

    .input-search {
      border: none;
      border-bottom: 2px solid;
      width: 120px;
      margin-left: 120px;
      margin-bottom: 5px;

      &:focus {
        outline: none;
      }
    }
  }
}
</style>
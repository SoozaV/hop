<template>
  <b-container class="menu">
    <b-row>
      <b-col>
        <img
          :src="userAvatar"
          alt=""
          class="user-avatar"
          style="margin-top: 0"
        />
      </b-col>
    </b-row>
    <b-row>
      <b-col>
        <p class="h2 nombre">{{ nombre }}</p>
      </b-col>
    </b-row>
    <b-row class="menu-links">
      <b-col cols="12">
        <router-link to="/inbox">
          <p class="h2" style="margin-bottom: 0; display: inline-block">
            <b-icon icon="envelope-open"></b-icon>
          </p>
          Inbox
        </router-link>
      </b-col>
      <b-col cols="12">
        <router-link to="/">
          <p class="h2" style="margin-bottom: 0; display: inline-block">
            <b-icon icon="person"></b-icon>
          </p>
          Mi Perfil
        </router-link>
      </b-col>
      <b-col cols="12">
        <router-link to="/">
          <p class="h2" style="margin-bottom: 0; display: inline-block">
            <img :src="logo" class="hop-logo black" />
          </p>
          Mi Home Office
        </router-link>
      </b-col>
      <b-col cols="12">
        <router-link to="/">
          <p class="h2" style="margin-bottom: 0; display: inline-block">
            <b-icon icon="bell"></b-icon>
          </p>
          Mis Solicitudes
        </router-link>
      </b-col>
      <b-col cols="12">
        <router-link to="/">
          <p class="h2" style="margin-bottom: 0; display: inline-block">
            <b-icon icon="box-arrow-left"></b-icon>
          </p>
          Log Out
        </router-link>
      </b-col>
    </b-row>
    <Footer />
  </b-container>
</template>

<script>
// @ is an alias to /src
import Footer from "@/components/Footer.vue";

export default {
  name: "Menu",
  components: {
    Footer,
  },
  data() {
    return {
      userAvatar: require("../assets/img/user@4x.webp"),
      logo: require("../assets/img/HOP@2x.webp"),
      nombre: "Raul Carmona Chaltelt",
    };
  },
};
</script>

<style lang="scss">
.menu {
  padding-top: 98px;
  .user-avatar {
    width: 120px;
    max-width: 90%;
    margin: 70px 0 45px;
  }
  .nombre {
    color: #1d1d1d;
    font-size: 20px;
    font-family: "Montserrat", sans-serif;
    font-weight: bold;
    margin-bottom: 35px;
  }
  .menu-links {
    .col-12 {
      display: flex;
      justify-content: flex-start;
      .hop-logo.black {
        filter: invert(1);
        max-width: 24.56px;
      }
      a {
        color: #1d1d1d;
        font-size: 15px;
        font-family: "Montserrat", sans-serif;
        text-decoration: none;
        display: flex;
        align-items: center;
        margin: 5px 0;
        p {
          margin-right: 15px;
        }
      }
    }
  }
}
</style>

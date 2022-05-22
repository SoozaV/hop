<template>
  <b-col :lg="col" class="side-menu">
    <b-container>
      <b-row>
        <b-col class="d-flex justify-content-start">
          <img
            :src="require('../assets/img/user@4x.webp')"
            alt=""
            class="user-avatar"
            style="margin-top: 0"
          />
        </b-col>
      </b-row>
      <b-row>
        <b-col>
          <p class="h2 nombre">@Raul0077</p>
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
          <router-link to="/perfil">
            <p class="h2" style="margin-bottom: 0; display: inline-block">
              <b-icon icon="person"></b-icon>
            </p>
            Mi Perfil
          </router-link>
        </b-col>
        <b-col cols="12">
          <router-link to="/miHomeOffice">
            <p class="h2" style="margin-bottom: 0; display: inline-block">
              <img :src="logo" class="hop-logo black" />
            </p>
            Mi Home Office
          </router-link>
        </b-col>
        <b-col cols="12">
          <router-link to="/solicitudes">
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
    </b-container>
  </b-col>
</template>

<script>
export default {
  name: "SideMenu",
  props: {
    col: {
      type: Number,
      default: 4
    }
  },
  data() {
    return {
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
.side-menu {
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
    text-align: left;
  }
  .menu-links {
    max-width: 620px !important;
    margin: 0 auto;
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
@media screen and (max-width: 991px) {
  .side-menu {
        display: none;
  }
}
</style>

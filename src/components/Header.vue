<template>
  <div id="nav">
    <b-row>
      <b-col cols="4" style="text-align: left">
        <router-link to="/">
          <img
            :src="logo"
            class="hop-logo"
            v-bind:class="{ white: $route.name === 'Home' }"
          />
        </router-link>
      </b-col>
      <b-col
        class="col menu-col"
        v-bind:class="{ white: $route.name === 'Home' }"
        style="display: flex; justify-content: flex-end"
      >
        <router-link v-if="$route.name === 'Home'" to="/login">
          Log In
        </router-link>
        <router-link v-if="$route.name === 'Home'" to="/signup">
          Sign Up
        </router-link>
        <router-link to="/menu"
          ><p class="h2" style="margin-bottom: 0">
            <b-icon icon="list"></b-icon></p
        ></router-link>
      </b-col>
    </b-row>
  </div>
</template>
<script>
export default {
  data() {
    return {
      logo: require("../assets/img/HOP@2x.webp"),
    };
  },
};
</script>
<style lang="scss">
#nav {
  width: 100%;
  padding: 30px;
  position: absolute;
  .hop-logo {
    width: 48px;
    filter: invert(1) !important;
    &.white {
      filter: invert(0) !important;
    }
  }
  .menu-col {
    align-items: center;
    &.white {
      a {
        color: white;
        text-decoration: none;
        font-family: "Montserrat", sans-serif;
        font-size: 12px;
        &:not(:last-child) {
          margin-right: 20px;
        }
      }
    }
    a {
      font-weight: bold;
      color: #2c3e50;

      &.router-link-exact-active {
        color: #42b983;
      }
    }
  }
}
</style>

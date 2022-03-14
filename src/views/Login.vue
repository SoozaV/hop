<template>
  <b-container class="sign-up">
    <b-row class="sign-buttons">
      <b-col style="text-align: right">
        <router-link
          class="btn hop-btn sign-btn login-btn shadow-none"
          to="/login"
          >Login</router-link
        >
      </b-col>
      <b-col style="text-align: left">
        <router-link
          class="btn hop-btn sign-btn signUp-btn shadow-none"
          to="/signup"
          >Sign Up</router-link
        >
      </b-col>
    </b-row>
    <b-row align-h="center" style="margin-top: 40px">
      <b-col lg="7">
        <b-form>
          <b-row class="form-field-container sign-user mx-auto">
            <b-col>
              <b-form-group
                id="input-group-email"
                label="Username or Email"
                label-for="input-email"
                label-align="left"
              >
                <!-- Email -->
                <b-form-input
                  id="input-email"
                  type="email"
                  class="shadow-none"
                  placeholder="Email"
                  required
                ></b-form-input>
              </b-form-group>
            </b-col>
          </b-row>
          <b-row class="form-field-container sign-user mx-auto">
            <b-col>
              <b-form-group
                id="input-group-password"
                label="Password"
                label-for="input-password"
                label-align="left"
              >
                <!-- Password -->
                <b-form-input
                  id="input-password"
                  type="password"
                  class="shadow-none"
                  placeholder="Password"
                  required
                ></b-form-input>
              </b-form-group>
            </b-col>
          </b-row>

          <b-row>
            <b-col>
              <b-button
                type="submit"
                class="hop-btn sign-btn block shadow-none"
                style="margin-right: 5px"
              >
                Log In
              </b-button>
            </b-col>
          </b-row>
        </b-form>
      </b-col>
    </b-row>
    <b-row class="social-login-section">
      <b-col>
        <h4>Log in with</h4>
        <p>Or click below to sign-in to your account</p>
      </b-col>
      <b-col class="col social-login-col">
        <button>
          <img :src="facebookBtn" alt="Facebook Login" />
        </button>
        <button>
          <img :src="googleBtn" alt="Facebook Login" />
        </button>
      </b-col>
    </b-row>
    <Footer />
  </b-container>
</template>

<script>
// @ is an alias to /src
import Footer from "@/components/Footer.vue";

export default {
  name: "SignUp",
  components: {
    Footer,
  },
  data() {
    return {
      facebookBtn: require("../assets/img/facebook@2x.png"),
      googleBtn: require("../assets/img/google@2x.png"),
      selected: {
        idioma: null,
        pais: null,
        profesion: null,
        intereses: null,
      },
    };
  },
};
</script>

<style lang="scss">
.sign-up {
  padding-top: 98px;
  .form-field-container {
    &.sign-user {
      border: 0;
      border-radius: 0;
      .form-group {
        border-bottom: 1px solid;
      }
    }
  }
  .sign-btn {
    border-radius: 10px;
    font-size: 20px;
    padding: 19px 0;
    &.block {
      width: 90%;
    }
    &.login-btn,
    &.signUp-btn {
      font-size: 15px;
      width: 116px;
      max-width: 116px;
      border: 1px solid #fcca2e;
      margin-top: 0;
    }
    &.login-btn {
      background-color: white !important;
      border: 1px solid;
    }
  }
  .social-login-section {
    margin: 50px auto 10px;
    max-width: 920px!important;
    h4 {
      font-family: "Montserrat", sans-serif;
      font-size: 15px;
      font-weight: bold;
      text-align: left;
    }
    p {
      font-family: "Montserrat", sans-serif;
      text-align: left;
      font-size: 12px;
      color: #b5b5b5;
    }
    .social-login-col {
      display: flex;
      justify-content: flex-end;
      button {
        background: transparent;
        border: none;
        outline: none;
        img {
          width: 50px;
        }
      }
    }
  }
}
</style>

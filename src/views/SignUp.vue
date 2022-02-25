<template>
  <b-container class="sign-up">
    <b-row class="sign-buttons">
      <b-col style="text-align: right;">
        <router-link class="btn hop-btn sign-btn login-btn shadow-none" to="/login">Login</router-link>
      </b-col>
      <b-col style="text-align: left;">
        <router-link class="btn hop-btn sign-btn signUp-btn shadow-none" to="/signup">Sign Up</router-link>
      </b-col>
    </b-row>
    <b-row>
      <b-col>
        <b-form>
          <b-row class="form-field-container sign-user mx-auto">
            <b-col>
              <img :src="userAvatar" alt="" class="user-avatar" />
            </b-col>
          </b-row>
          <b-row class="form-field-container sign-user mx-auto">
            <b-col>
              <b-form-group
                id="input-group-nombre"
                label="Nombre"
                label-for="input-nombre"
                label-align="left"
              >
                <!-- Nombre -->
                <b-form-input
                  id="input-nombre"
                  type="text"
                  class="shadow-none"
                  placeholder="Nombre"
                  required
                ></b-form-input>
              </b-form-group>
            </b-col>
          </b-row>
          <b-row class="form-field-container sign-user mx-auto">
            <b-col>
              <b-form-group
                id="input-group-apellidos"
                label="Apellidos"
                label-for="input-apellidos"
                label-align="left"
              >
                <!-- Apellidos -->
                <b-form-input
                  id="input-apellidos"
                  type="text"
                  class="shadow-none"
                  placeholder="Apellidos"
                  required
                ></b-form-input>
              </b-form-group>
            </b-col>
          </b-row>
          <b-row class="form-field-container sign-user mx-auto">
            <b-col>
              <b-form-group
                id="input-group-email"
                label="Email"
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
          <b-row class="form-field-container sign-user mt-2 mx-auto">
            <b-col>
              <b-form-group
                id="input-group-idioma"
                label-for="input-idioma"
                label-align="left"
                class="custom-select"
              >
                <!-- Idioma -->
                <b-form-select
                  onfocus="this.size=5;"
                  onblur="this.size=1;"
                  onchange="this.size=1; this.blur();"
                  onfocusout="this.size=null;"
                  v-model="selected.idioma"
                  :options="[{ value: null, text: 'Idioma' }, 1, 2, 3, 4]"
                ></b-form-select>
              </b-form-group>
            </b-col>
            <b-col>
              <b-form-group
                id="input-group-pais"
                label-for="input-pais"
                label-align="left"
                class="custom-select"
              >
                <!-- País -->
                <b-form-select
                  onfocus="this.size=5;"
                  onblur="this.size=1;"
                  onchange="this.size=1; this.blur();"
                  onfocusout="this.size=null;"
                  v-model="selected.pais"
                  :options="[{ value: null, text: 'País' }, 1, 2, 3, 4]"
                ></b-form-select>
              </b-form-group>
            </b-col>
          </b-row>
          <b-row class="form-field-container sign-user mt-2 mx-auto">
            <b-col>
              <b-form-group
                id="input-group-telefono"
                label="Teléfono"
                label-for="input-telefono"
                label-align="left"
                class="custom-select"
              >
                <!-- Teléfono -->
                <b-form-input
                  id="input-telefono"
                  type="text"
                  class="shadow-none"
                  placeholder="Teléfono"
                  required
                ></b-form-input>
              </b-form-group>
            </b-col>
            <b-col>
              <b-form-group
                id="input-group-nacimiento"
                label="Fecha de nacimiento"
                label-for="input-nacimiento"
                label-align="left"
                class="birthday"
              >
                <!-- Fecha de nacimiento día -->
                <b-form-input
                  id="input-nacimiento-dia"
                  type="text"
                  class="shadow-none"
                  placeholder="DD"
                  maxlength="2"
                  size="2"
                  required
                ></b-form-input>

                <!-- Fecha de nacimiento mes -->
                <b-form-input
                  id="input-nacimiento-mes"
                  type="text"
                  class="shadow-none"
                  placeholder="MM"
                  maxlength="2"
                  size="2"
                  required
                ></b-form-input>

                <!-- Fecha de nacimiento año -->
                <b-form-input
                  id="input-nacimiento-anio"
                  type="text"
                  class="shadow-none"
                  placeholder="AAAA"
                  maxlength="4"
                  size="4"
                  required
                ></b-form-input>
              </b-form-group>
            </b-col>
          </b-row>
          <b-row class="form-field-container sign-user mt-2 mx-auto">
            <b-col>
              <b-form-group
                id="input-group-1"
                label-for="input-1"
                label-align="left"
                class="custom-select"
              >
                <!-- Profesión -->
                <b-form-select
                  onfocus="this.size=5;"
                  onblur="this.size=1;"
                  onchange="this.size=1; this.blur();"
                  onfocusout="this.size=null;"
                  v-model="selected.profesion"
                  :options="[{ value: null, text: 'Profesión' }, 1, 2, 3, 4]"
                ></b-form-select>
              </b-form-group>
            </b-col>
            <b-col>
              <b-form-group
                id="input-group-1"
                label-for="input-1"
                label-align="left"
                class="custom-select"
              >
                <!-- Intereses -->
                <b-form-select
                  onfocus="this.size=5;"
                  onblur="this.size=1;"
                  onchange="this.size=1; this.blur();"
                  onfocusout="this.size=null;"
                  v-model="selected.intereses"
                  :options="[{ value: null, text: 'Intereses' }, 1, 2, 3, 4]"
                ></b-form-select>
              </b-form-group>
            </b-col>
          </b-row>
          <b-row class="form-field-container sign-user mt-2 mx-auto">
            <b-col>
              <b-form-group
                id="input-group-about"
                label="Acerca de mi"
                label-for="input-about"
                label-align="left"
              >
                <b-form-textarea
                  id="textarea-about"
                  placeholder="Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut viverra sodales efficitur. Donec ultrices id mi nec imperdiet. Proin turpis est, aliquet sit amet neque placerat, vestibulum interdum metus. Mauris vita"
                  rows="5"
                  class="shadow-none"
                  no-resize
                ></b-form-textarea>
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
                Sign Up
              </b-button>
            </b-col>
          </b-row>
        </b-form>
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
      userAvatar: require("../assets/img/user@4x.webp"),
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
      .user-avatar {
        width: 120px;
        max-width: 90%;
        margin: 70px 0 45px;
      }
      .form-group {
        border-bottom: 1px solid;
        &.birthday {
          border: 0;
          border-bottom: 1px solid;
          div {
            display: flex;
            justify-content: space-between;
            input {
              max-width: 20%;
              //border-bottom: 1px solid;
              border-radius: 0;
              text-align: center;
              &:last-child {
                max-width: 40%;
              }
            }
          }
        }
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
    &.login-btn, &.signUp-btn {
      font-size: 15px;
      width: 116px;
      max-width: 116px;
      border: 1px solid #fcca2e;
      margin-top: 0;
    }
    &.login-btn {
      background-color: white!important;
      border: 1px solid;
    }
  }
}

</style>

<template>
  <b-container class="perfil">
    <b-row>
      <SideMenu />
      <b-col>
        <b-form>
          <b-row class="form-field-container sign-user mx-auto">
            <b-col>
              <img :src="userAvatar" alt="" class="user-avatar" />
            </b-col>
          </b-row>
          <b-row>
            <b-col>
              <p class="h2 nombre">{{ nombre }}</p>
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
                  v-model="email"
                  placeholder="Email"
                  disabled
                  required
                ></b-form-input>
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
                  v-model="telefono"
                  required
                  disabled
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
                  placeholder=""
                  v-model="nacimiento"
                  required
                  disabled
                ></b-form-input>
              </b-form-group>
            </b-col>
          </b-row>

          <b-row class="form-field-container sign-user mx-auto">
            <b-col>
              <b-form-group
                id="input-group-idiomas"
                label="Idiomas"
                label-for="input-idiomas"
                label-align="left"
                class="tags"
              >
                <b-button type="submit" class="hop-btn perfil-btn shadow-none"
                  >Español</b-button
                >
                <b-button type="submit" class="hop-btn perfil-btn shadow-none"
                  >Inglés</b-button
                >
                <b-button type="submit" class="hop-btn perfil-btn shadow-none"
                  >Francés</b-button
                >
              </b-form-group>
            </b-col>
          </b-row>

          <b-row class="form-field-container sign-user mx-auto">
            <b-col>
              <b-form-group
                id="input-group-profesion"
                label="Profesión"
                label-for="input-profesion"
                label-align="left"
              >
                <!-- Profesión -->
                <b-form-input
                  id="input-profesion"
                  type="text"
                  class="shadow-none"
                  placeholder="Profesión"
                  v-model="profesion"
                  disabled
                  required
                ></b-form-input>
              </b-form-group>
            </b-col>
          </b-row>

          <b-row class="form-field-container sign-user mx-auto">
            <b-col>
              <b-form-group
                id="input-group-intereses"
                label="Intereses"
                label-for="input-intereses"
                label-align="left"
                class="tags"
              >
                <b-button type="submit" class="hop-btn perfil-btn shadow-none"
                  >Emprendedor</b-button
                >
                <b-button type="submit" class="hop-btn perfil-btn shadow-none"
                  >Viajero</b-button
                >
                <b-button type="submit" class="hop-btn perfil-btn shadow-none"
                  >Amable</b-button
                >
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
                  placeholder=""
                  rows="6"
                  class="shadow-none"
                  v-model="about"
                  disabled
                  no-resize
                ></b-form-textarea>
              </b-form-group>
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
import SideMenu from "@/components/SideMenu.vue";

export default {
  name: "Perfil",
  components: {
    Footer,
    SideMenu
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
      nombre: "Raul Carmona Chaltelt",
      email: "raul@homeofficepartner.mx",
      telefono: "52 11 22 33 44",
      nacimiento: "28 Febrero 1990",
      profesion: "Ingeniero Industrial",
      about: "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut viverra sodales efficitur. Donec ultrices id mi nec imperdiet. Proin turpis est, aliquet sit amet neque placerat, vestibulum interdum metus. Mauris vita"
    };
  },
};
</script>

<style lang="scss">
.perfil {
  padding-top: 98px;
  .nombre {
    color: #1d1d1d;
    font-size: 20px;
    font-family: "Montserrat", sans-serif;
    font-weight: bold;
    margin-bottom: 35px;
  }
  .form-field-container {
    &.sign-user {
      border: 0;
      border-radius: 0;
      .user-avatar {
        width: 120px;
        max-width: 90%;
        margin: 0 0 45px;
      }
      .form-group {
        margin-bottom: 11px;
        label {
          color: #b5b5b5;
          margin-bottom: 7px;
        }
        input, textarea {
          font-size: 15px;
          font-family: "Montserrat", sans-serif;
          font-weight: bold;
          color: #1d1d1d;
          &:disabled {
            background: transparent;
          }
        }
        &.tags div {
          display: flex;
          .perfil-btn {
            margin-top: 0;
            padding: 5px 16px;
            &:not(:last-child) {
              margin-right: 10px;
            }
          }
        }
      }
    }
  }
}
</style>

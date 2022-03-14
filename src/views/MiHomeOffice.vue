<template>
  <b-container class="mi-home-office">
    <b-row align-h="center">
      <b-col lg="8">
        <b-form>
          <b-row class="form-field-container sign-user mx-auto mb-5">
            <b-col>
              <img :src="imagenPrincipal" alt="" class="banner-mho mb-0" />
              <div class="count shadow">
                <div class="number">2</div>
                <div class="text">Días<br />restantes</div>
              </div>
            </b-col>
          </b-row>
          <b-row align-h="center">
            <b-col cols="6" sm="6" lg="4" class="mho-title">
              <h2>Grat<br />Co-Working</h2>
            </b-col>
            <b-col
              cols="6"
              sm="6"
              lg="4"
              class="rank-col"
              style="flex-wrap: wrap"
            >
              <div class="rank">3.0</div>
              <div class="stars">
                <b-img :src="star" alt="" />
                <b-img :src="star" alt="" />
                <b-img :src="star" alt="" />
                <b-img :src="star" alt="" />
                <b-img :src="star" alt="" />
              </div>
              <h3>Emilio Castelar #83</h3>
              <div class="separador"></div>
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

          <b-row class="form-field-container sign-user mx-auto">
            <b-col>
              <b-form-group
                id="input-group-reglas"
                label="Reglas"
                label-for="input-reglas"
                label-align="left"
                class="tags"
              >
                <b-button type="submit" class="hop-btn perfil-btn shadow-none"
                  >No fumar</b-button
                >
                <b-button type="submit" class="hop-btn perfil-btn shadow-none"
                  >No niños</b-button
                >
              </b-form-group>
            </b-col>
          </b-row>

          <b-row class="form-field-container sign-user mx-auto">
            <b-col>
              <b-form-group
                id="input-group-areas"
                label="Áreas comunes"
                label-for="input-areas"
                label-align="left"
                class="tags"
              >
                <b-button type="submit" class="hop-btn perfil-btn shadow-none"
                  >Terraza</b-button
                >
              </b-form-group>
            </b-col>
            <b-col>
              <b-form-group
                id="input-group-servicios"
                label="Áreas comunes"
                label-for="input-servicios"
                label-align="left"
                class="tags"
              >
                <b-button type="submit" class="hop-btn perfil-btn shadow-none"
                  >Cafetería</b-button
                >
                <b-button type="submit" class="hop-btn perfil-btn shadow-none"
                  >Internet</b-button
                >
              </b-form-group>
            </b-col>
          </b-row>

          <b-row class="form-field-container sign-user mt-2 mx-auto">
            <b-col>
              <b-calendar
                class="shadow-none"
                locale="es-Es"
                :hide-header="false"
              ></b-calendar>
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
  name: "MiHomeOffice",
  components: {
    Footer,
  },
  data() {
    return {
      star: require("../assets/img/star@4x.webp"),
      imagenPrincipal: require("../assets/img/office.png"),
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
      about:
        "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut viverra sodales efficitur. Donec ultrices id mi nec imperdiet. Proin turpis est, aliquet sit amet neque placerat, vestibulum interdum metus. Mauris vita",
    };
  },
};
</script>

<style lang="scss">
.mi-home-office {
  padding-top: 98px;

  .count {
    display: flex;
    position: relative;
    background: white;
    border-radius: 15px;
    width: 50%;
    max-width: 190px;
    justify-content: center;
    align-items: center;
    margin: -30px auto 0;
    padding: 7px 0;
    .number {
      width: 40%;
      color: #1d1d1d;
      text-align: center;
      font-size: 33px;
      font-weight: bold;
      font-family: "Montserrat", sans-serif;
    }
    .text {
      width: 60%;
      text-align: left;
      font-family: "Montserrat", sans-serif;
      font-size: 12px;
      padding-left: 12px;
      position: relative;
      &:before {
        content: "";
        height: 100%;
        width: 1px;
        background: #9c9c9c;
        position: absolute;
        left: 0;
      }
      &:after {
        content: "";
        width: 10px;
        height: 10px;
        border-radius: 100%;
        background: #33c410;
        position: absolute;
        top: -6px;
        right: 8px;
      }
    }
  }
  .separador {
    background: #1d1d1d;
    width: 32px;
    height: 3px;
    margin-bottom: 16px;
  }
  .mho-title {
    color: #1d1d1d;
    text-align: left;
    font-size: 20px;
    font-family: "Montserrat", sans-serif;
    h2 {
      font-weight: bold;
    }
  }
  .rank-col {
    display: flex;
    justify-content: space-between;
    margin-bottom: 12px;
    //flex-wrap: wrap;
    h3 {
      width: 100%;
      text-align: left;
      font-family: "Montserrat", sans-serif;
      font-size: 12px;
      color: #1d1d1d;
      margin-top: 10px;
      margin-bottom: 10px;
    }
    .rank {
      font-family: "Montserrat", sans-serif;
      font-weight: bold;
      font-size: 12px;
    }
    .stars {
      display: flex;
      img {
        width: 15px;
        height: 15px;
      }
    }
  }
  .form-field-container {
    &.sign-user {
      border: 0;
      border-radius: 0;
      .banner-mho {
        width: 100%;
        margin: 0 0 45px;
        border-radius: 20px;
      }
      .form-group {
        margin-bottom: 11px;
        label {
          color: #b5b5b5;
          margin-bottom: 7px;
        }
        input,
        textarea {
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

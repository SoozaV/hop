<template>
  <b-container class="home-search">
    <b-row>
      <b-col class="carousel">
        <h2 class="text-center mb-5">Tenemos una opción para ti</h2>
        <carousel
          :loop="true"
          :dots="false"
          :nav="false"
          :responsive="{
            980: { items: 4, margin: 25 },
            640: { items: 3, margin: 17 },
            0: { items: 2.5, margin: 10 },
          }"
        >
          <b-card
            title="1"
            :img-src="require('@/assets/img/slider-1@2x.png')"
            img-alt="Image"
            img-top
            tag="article"
            class="mb-2"
          >
            <b-card-text> Crea tu perfil </b-card-text>
          </b-card>
          <b-card
            title="2"
            :img-src="require('@/assets/img/slider-2@2x.png')"
            img-alt="Image"
            img-top
            tag="article"
            class="mb-2"
          >
            <b-card-text> Encuentra un Home Office a tu medida </b-card-text>
          </b-card>
          <b-card
            title="3"
            :img-src="require('@/assets/img/slider-3@2x.png')"
            img-alt="Image"
            img-top
            tag="article"
            class="mb-2"
          >
            <b-card-text>
              Conecta con tu Home Office Partner Ideal
            </b-card-text>
          </b-card>
          <b-card
            title="4"
            :img-src="require('@/assets/img/slider-4@2x.png')"
            img-alt="Image"
            img-top
            tag="article"
            class="mb-2"
          >
            <b-card-text> Comparte experiencias </b-card-text>
          </b-card>
        </carousel>
      </b-col>
    </b-row>
    <b-row>
      <b-col>
        <h2>Comparte experiencias</h2>
        <h3>Conecta con tu home office partner ideal.</h3>
      </b-col>
    </b-row>
    <b-row>
      <b-col>
        <b-form>
          <b-row class="form-field-container mt-3 mx-auto">
            <b-col>
              <b-form-group
                id="input-group-1"
                label="Ubicación"
                label-for="input-1"
                label-align="left"
              >
                <!-- Ubicación -->
                <b-form-input
                  id="input-1"
                  type="text"
                  class="shadow-none"
                  placeholder="Cerca de aquí"
                  required
                ></b-form-input>
              </b-form-group>
            </b-col>
          </b-row>
          <b-row class="form-field-container mt-2 mx-auto">
            <b-col>
              <b-form-group
                id="input-group-1"
                label="Disponibilidad"
                label-for="input-1"
                label-align="left"
                class="custom-select"
              >
                <!-- Horario -->
                <b-form-select
                  onfocus="this.size=5;"
                  onblur="this.size=1;"
                  onchange="this.size=1; this.blur();"
                  onfocusout="this.size=null;"
                  v-model="selected.disponibilidad"
                  :options="optionsDisponibilidad"
                ></b-form-select>
              </b-form-group>
            </b-col>
            <b-col class="right-form-col col">
              <b-form-group
                id="input-group-1"
                label="Tipo de espacio"
                label-for="input-1"
                label-align="left"
                class="custom-select"
              >
                <!-- Características -->
              </b-form-group>
            </b-col>
          </b-row>
          <b-row>
            <b-col>
              <b-button
                to="/search"
                type="submit"
                class="hop-btn shadow-none"
                style="margin-right: 5px"
              >
                Búsqueda
              </b-button>
            </b-col>
          </b-row>
        </b-form>
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
import carousel from "vue-owl-carousel";

export default {
  name: "HomeSearchSection",
  components: {
    carousel,
  },
  data() {
    return {
      rangeValue: "500",
      advancedSymbol: "+",
      selected: {
        disponibilidad: null,
        caracteristicas: null,
        presupuesto: null,
        intereses: null,
        areasComunes: null,
        reglas: null,
        servicios: null,
        interesesPartners: null,
      },
      optionsDisponibilidad: [
        { value: null, text: "Tipos de horario" },
        { value: "a", text: "Opción 1" },
        { value: "b", text: "Opción 2" },
        { value: "c", text: "Opción 3" },
        { value: "d", text: "Opción 4" },
      ],
      optionsCaracteristicas: [
        { value: null, text: "Tipos de espacio" },
        { value: "a", text: "Opción 1" },
        { value: "b", text: "Opción 2" },
        { value: "c", text: "Opción 3" },
        { value: "d", text: "Opción 4" },
      ],
      optionsPresupuesto: [
        { value: null, text: "$ - $$$" },
        { value: "a", text: "Opción 1" },
        { value: "b", text: "Opción 2" },
        { value: "c", text: "Opción 3" },
        { value: "d", text: "Opción 4" },
      ],
      optionsIntereses: [
        { value: null, text: "Acerca de ti" },
        { value: "a", text: "Opción 1" },
        { value: "b", text: "Opción 2" },
        { value: "c", text: "Opción 3" },
        { value: "d", text: "Opción 4" },
      ],
      optionsAreas: [
        { value: null, text: "Qué incluye" },
        { value: "a", text: "Opción 1" },
        { value: "b", text: "Opción 2" },
        { value: "c", text: "Opción 3" },
        { value: "d", text: "Opción 4" },
      ],
      optionsReglas: [
        { value: null, text: "Qué se permite" },
        { value: "a", text: "Opción 1" },
        { value: "b", text: "Opción 2" },
        { value: "c", text: "Opción 3" },
        { value: "d", text: "Opción 4" },
      ],
      optionsServicios: [
        { value: null, text: "Qué incluye" },
        { value: "a", text: "Opción 1" },
        { value: "b", text: "Opción 2" },
        { value: "c", text: "Opción 3" },
        { value: "d", text: "Opción 4" },
      ],
      optionsPartners: [
        { value: null, text: "Tipos de partners" },
        { value: "a", text: "Opción 1" },
        { value: "b", text: "Opción 2" },
        { value: "c", text: "Opción 3" },
        { value: "d", text: "Opción 4" },
      ],
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
.home-search {
  margin: 0 auto;
  max-width: 920px !important;
  padding-top: 20px;
  .carousel {
    margin-top: 44px;
    margin-bottom: 44px;
    .owl-item {
      border-radius: 20px;
      article {
        border-radius: 20px;
        min-height: 360px;

        border: 0;
        .card-body {
          background: #fcca2e;
          border-radius: 0 0 20px 20px;
          font-family: "Montserrat", sans-serif;
          color: #1d1d1d;
          font-weight: 800;
          .card-title {
            border: 1px solid #707070;
            border-radius: 100px;
            width: 78px;
            height: 78px;
            display: flex;
            justify-content: center;
            align-items: center;
            margin: auto;
            font-family: "Montserrat", sans-serif;
            color: #1d1d1d;
            font-weight: 800;
            margin-bottom: 15px;
          }
        }
      }
    }
  }
  .row {
    .col {
      h2,
      h3 {
        text-align: left;
        font-family: "Montserrat", sans-serif;
        color: #1d1d1d;
        font-weight: 800;
        font-size: 20px;
      }
      h3 {
        font-size: 12px;
        font-weight: 400;
        line-height: 1.4em;
      }
    }
  }
}
.form-field-container {
  border: 1px solid #1d1d1d;
  padding: 9px 2px 5px;
  border-radius: 10px;
  max-width: 100%;
  label {
    font-family: "Montserrat", sans-serif;
    font-size: 10px;
    text-transform: uppercase;
    font-weight: bold;
    &.text-left {
      text-align: left;
    }
  }
  input,
  textarea {
    padding: 0;
    border: 0;
    font-family: "Montserrat", sans-serif;
  }
  .right-form-col {
    border-left: 1px solid;
  }
  .col {
    .custom-select {
      div {
        position: relative;
        select {
          width: 100%;
          border: 0;
          outline: none;
          font-family: "Montserrat", sans-serif;
          color: #1d1d1d;
          background: none;
          &:focus {
            background: white;
            position: absolute;
            width: 200%;
            left: 0;
            padding: 5px;
            border: 1px solid #1d1d1d;
            border-radius: 10px;
            color: #b5b5b5;
            z-index: 50;
            option {
              &:hover {
                color: #1d1d1d;
              }
            }
          }
        }
      }
    }
  }
}
.btn.hop-btn {
  background-color: #fcca2e !important;
  font-family: "Montserrat", sans-serif;
  border: 0;
  color: #1d1d1d !important;
  font-size: 12px;
  border-radius: 50px;
  margin-top: 39px;
  padding: 9px 33px;
  &.advanced {
    padding: 9px 15px;
    margin-left: 5px;
  }
}
@media screen and (max-width: 480px) {
  .home-search {
    .carousel {
      .owl-item {
        article {
          min-height: 260px;
          .card-body {
            font-size: 12px;
            .card-title {
              width: 35px;
              height: 35px;
              font-size: 14px;
            }
          }
        }
      }
    }
  }
}
</style>

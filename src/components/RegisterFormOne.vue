<template>
  <b-container class="register-form">
    <b-row>
      <b-col cols="12" lg="8" class="col" style="margin: 0 auto !important">
        <h2 class="mt-3 mb-4" style="text-align: center">
          Confirma tu dirección
        </h2>
      </b-col>
    </b-row>
    <b-row>
      <b-col cols="12" lg="8" style="margin: 0 auto !important">
        <b-form>
          <div class="register-box">
            <b-row class="form-field-container mx-auto">
              <b-col>
                <b-form-group
                  id="input-group-calle"
                  label="Calle"
                  label-for="input-calle"
                  label-align="left"
                >
                  <!-- Calle -->
                  <b-form-input
                    id="input-calle"
                    type="text"
                    class="shadow-none"
                    placeholder="Lorem ipsum"
                    required
                  ></b-form-input>
                </b-form-group>
              </b-col>
            </b-row>
            <b-row class="form-field-container mx-auto">
              <b-col>
                <b-form-group
                  id="input-group-numero"
                  label="Número"
                  label-for="input-numero"
                  label-align="left"
                  class="custom-select"
                >
                  <!-- Número -->
                  <b-form-input
                    id="input-numero"
                    type="text"
                    class="shadow-none"
                    placeholder="Depto., suite, etc. (Opcional)"
                    required
                  ></b-form-input>
                </b-form-group>
              </b-col>
            </b-row>
            <b-row class="form-field-container mx-auto">
              <b-col class="col">
                <b-form-group
                  id="input-group-ciudad"
                  label="Ciuedad"
                  label-for="input-ciudad"
                  label-align="left"
                  class="custom-select"
                >
                  <!-- Ciudad -->
                  <b-form-input
                    id="input-ciudad"
                    type="text"
                    class="shadow-none"
                    placeholder="Veracruz"
                    required
                  ></b-form-input>
                </b-form-group>
              </b-col>
            </b-row>
            <b-row class="form-field-container mx-auto">
              <b-col class="col">
                <b-form-group
                  id="input-group-estado"
                  label="Estado"
                  label-for="input-estado"
                  label-align="left"
                  class="custom-select"
                >
                  <!-- Estado -->
                  <b-form-input
                    id="input-estado"
                    type="text"
                    class="shadow-none"
                    placeholder="Veracruz"
                    required
                  ></b-form-input>
                </b-form-group>
              </b-col>
            </b-row>
            <b-row class="form-field-container mx-auto">
              <b-col class="col">
                <b-form-group
                  id="input-group-zip"
                  label="Código Postal"
                  label-for="input-zip"
                  label-align="left"
                  class="custom-select"
                >
                  <!-- Código Postal -->
                  <b-form-input
                    id="input-zip"
                    type="text"
                    class="shadow-none"
                    placeholder="91919"
                    required
                  ></b-form-input>
                </b-form-group>
              </b-col>
            </b-row>
            <b-row class="form-field-container mx-auto">
              <b-col class="col">
                <b-form-group
                  id="input-group-pais"
                  label="País o región"
                  label-for="input-pais"
                  label-align="left"
                  class="custom-select"
                >
                  <!-- Características -->
                  <b-form-input
                    id="input-pais"
                    type="text"
                    class="shadow-none"
                    placeholder="México - MX"
                    required
                  ></b-form-input>
                </b-form-group>
              </b-col>
            </b-row>
          </div>
          <b-row>
            <b-col>
              <h3 class="advice">
                Sólo compartiremos tu dirección con los Partners que tengan una
                reservación Confirmada, como se describe en nuestra
                <a href="#">política de privacidad</a>
              </h3>
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
                De acuerdo
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
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
.register-form {
  margin: 0 auto !important;
  max-width: 920px !important;
  padding-top: 20px;
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
        &.advice {
          color: #707070;
          font-size: 14px;
          margin-top: 10px;
          a {
            font-weight: bold;
            text-decoration: none;
            color: black;
          }
        }
      }
    }
  }
}
.register-form {
  .form-field-container {
    &:first-child {
      border-radius: 15px 15px 0 0;
    }
    &:last-child {
      border-radius: 0 0 15px 15px;
    }
    border-color: #707070;
    padding: 9px 2px 5px;
    border-radius: 0px;
    margin: 0;
    margin-top: -1px;
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
  .register-form {
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

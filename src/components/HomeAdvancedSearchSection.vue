<template>
  <b-container class="home-advanced-search">
    <b-row>
      <b-col>
        <h3 style="font-size: 16px" class="text-center">
          ${{ rangeValue }}.°°
        </h3>
        <b-form-input
          v-model="rangeValue"
          type="range"
          step="100"
          style="width: 100%; color: yellow"
          :min="rangeMin"
          :max="rangeMax"
        ></b-form-input>
        <div class="d-flex range-inputs justify-content-space-between">
          <label class="d-flex align-items-center"
            >Min
            <b-form-input
              id="range-min-input"
              type="text"
              v-model="rangeMin"
              class="shadow-none"
              placeholder="$2000"
            ></b-form-input
          ></label>
          <label class="d-flex align-items-center justify-content-end"
            >Max
            <b-form-input
              id="range-max-input"
              type="text"
              v-model="rangeMax"
              class="shadow-none"
              placeholder="$8000"
            ></b-form-input
          ></label>
        </div>
      </b-col>
    </b-row>
    <b-row>
      <b-col>
        <b-form>
          <b-row class="form-field-container mt-3 mx-auto">
            <b-col>
              <b-form-group
                id="input-group-1"
                label="Disponibilidad"
                label-for="input-1"
                label-align="left"
                class="custom-select"
              >
                <!-- Horario -->
                <b-dropdown
                  size="md"
                  text="Tipos de horario"
                  boundary="viewport"
                >
                  <b-form-checkbox name="checkbox-1">
                    Opción 1
                  </b-form-checkbox>
                  <b-form-checkbox name="checkbox-2">
                    Opción 2
                  </b-form-checkbox>
                  <b-form-checkbox name="checkbox-3">
                    Opción 3
                  </b-form-checkbox>
                </b-dropdown>
              </b-form-group>
            </b-col>
            <b-col class="right-form-col col">
              <b-form-group
                id="input-group-1"
                label="Tipo de edificio"
                label-for="input-1"
                label-align="left"
                class="custom-select"
              >
                <b-dropdown
                  size="md"
                  text="Características"
                  boundary="viewport"
                >
                  <b-form-checkbox name="checkbox-1">
                    Opción 1
                  </b-form-checkbox>
                  <b-form-checkbox name="checkbox-2">
                    Opción 2
                  </b-form-checkbox>
                  <b-form-checkbox name="checkbox-3">
                    Opción 3
                  </b-form-checkbox>
                </b-dropdown>
              </b-form-group>
            </b-col>
          </b-row>
          <b-row class="form-field-container mt-2 mx-auto">
            <b-col>
              <b-form-group
                id="input-group-1"
                label="Tipo de edificio"
                label-for="input-1"
                label-align="left"
                class="custom-select"
              >
                <b-dropdown
                  size="md"
                  text="Características"
                  boundary="viewport"
                >
                  <b-form-checkbox name="checkbox-1">
                    Opción 1
                  </b-form-checkbox>
                  <b-form-checkbox name="checkbox-2">
                    Opción 2
                  </b-form-checkbox>
                  <b-form-checkbox name="checkbox-3">
                    Opción 3
                  </b-form-checkbox>
                </b-dropdown>
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
                <b-dropdown
                  size="md"
                  text="Características"
                  boundary="viewport"
                >
                  <b-form-checkbox name="checkbox-1">
                    Opción 1
                  </b-form-checkbox>
                  <b-form-checkbox name="checkbox-2">
                    Opción 2
                  </b-form-checkbox>
                  <b-form-checkbox name="checkbox-3">
                    Opción 3
                  </b-form-checkbox>
                </b-dropdown>
              </b-form-group>
            </b-col>
          </b-row>

          <b-row class="form-field-container mt-2 mx-auto">
            <b-col>
              <b-form-group
                id="input-group-1"
                label="Áreas comunes"
                label-for="input-1"
                label-align="left"
                class="custom-select"
              >
                <b-dropdown
                  size="md"
                  text="Que incluye"
                  boundary="viewport"
                >
                  <b-form-checkbox name="checkbox-1">
                    Opción 1
                  </b-form-checkbox>
                  <b-form-checkbox name="checkbox-2">
                    Opción 2
                  </b-form-checkbox>
                  <b-form-checkbox name="checkbox-3">
                    Opción 3
                  </b-form-checkbox>
                </b-dropdown>
              </b-form-group>
            </b-col>
            <b-col class="right-form-col col">
              <b-form-group
                id="input-group-1"
                label="Servicios"
                label-for="input-1"
                label-align="left"
                class="custom-select"
              >
                <b-dropdown
                  size="md"
                  text="Que incluye"
                  boundary="viewport"
                >
                  <b-form-checkbox name="checkbox-1">
                    Opción 1
                  </b-form-checkbox>
                  <b-form-checkbox name="checkbox-2">
                    Opción 2
                  </b-form-checkbox>
                  <b-form-checkbox name="checkbox-3">
                    Opción 3
                  </b-form-checkbox>
                </b-dropdown>
              </b-form-group>
            </b-col>
          </b-row>
          <b-row class="form-field-container mt-2 mx-auto">
            <b-col>
              <b-form-group
                id="input-group-1"
                label="Reglas"
                label-for="input-1"
                label-align="left"
                class="custom-select"
              >
                <b-dropdown
                  size="md"
                  text="Que se permite"
                  boundary="viewport"
                >
                  <b-form-checkbox name="checkbox-1">
                    Opción 1
                  </b-form-checkbox>
                  <b-form-checkbox name="checkbox-2">
                    Opción 2
                  </b-form-checkbox>
                  <b-form-checkbox name="checkbox-3">
                    Opción 3
                  </b-form-checkbox>
                </b-dropdown>
              </b-form-group>
            </b-col>
            <b-col class="right-form-col col">
              <b-form-group
                id="input-group-1"
                label="Profesión de Partners"
                label-for="input-1"
                label-align="left"
                class="custom-select"
              >
                <b-dropdown
                  size="md"
                  text="Características partners"
                  boundary="viewport"
                >
                  <b-form-checkbox name="checkbox-1">
                    Opción 1
                  </b-form-checkbox>
                  <b-form-checkbox name="checkbox-2">
                    Opción 2
                  </b-form-checkbox>
                  <b-form-checkbox name="checkbox-3">
                    Opción 3
                  </b-form-checkbox>
                </b-dropdown>
              </b-form-group>
            </b-col>
          </b-row>
          <b-row class="form-field-container mt-2 mx-auto">
            <b-col>
                 <b-form-group
                id="input-group-1"
                label="Invitados"
                label-for="input-1"
                label-align="left"
                class="custom-select"
              >
                <b-dropdown
                  size="md"
                  text="Número de invitados"
                  boundary="viewport"
                >
                  <b-form-checkbox name="checkbox-1">
                    Opción 1
                  </b-form-checkbox>
                  <b-form-checkbox name="checkbox-2">
                    Opción 2
                  </b-form-checkbox>
                  <b-form-checkbox name="checkbox-3">
                    Opción 3
                  </b-form-checkbox>
                </b-dropdown>
              </b-form-group>
            </b-col>
            <b-col class="right-form-col col">
              <b-form-group
                id="input-group-1"
                label="Características de Partners"
                label-for="input-1"
                label-align="left"
                class="custom-select"
              >
                <b-dropdown
                  size="md"
                  text="Acerca de partners"
                  boundary="viewport"
                >
                  <b-form-checkbox name="checkbox-1">
                    Opción 1
                  </b-form-checkbox>
                  <b-form-checkbox name="checkbox-2">
                    Opción 2
                  </b-form-checkbox>
                  <b-form-checkbox name="checkbox-3">
                    Opción 3
                  </b-form-checkbox>
                </b-dropdown>
              </b-form-group>
            </b-col>
          </b-row>
          <b-row>
            <b-col>
              <b-button
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
export default {
  name: "HomeSearchSection",
  data() {
    return {
      rangeMin: "2000",
      rangeMax: "8000",
      rangeValue: "2500",
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
.home-advanced-search {
  margin: 0 auto;
  max-width: 920px !important;
  padding-top: 20px;
  /** FF*/
  input[type="range"]::-moz-range-progress {
    background-color: #fcca2e;
  }
  input[type="range"]::-moz-range-track {
    background-color: #efefef;
  }
  /* IE*/
  input[type="range"]::-ms-fill-lower {
    background-color: #fcca2e;
  }
  input[type="range"]::-ms-fill-upper {
    background-color: #efefef;
  }
  .range-inputs {
    margin: 20px 0 30px 0;
    & > label {
      color: #b5b5b5;
      font-family: "Montserrat", sans-serif;
      width: 50%;
      input {
        border: 2px solid #1d1d1d;
        border-radius: 5px;
        margin-left: 10px;
        width: 70px;
      }
    }
  }
  .b-dropdown {
    width: 100%;
    max-width: 100%;
    button.btn {
      text-align: left;
      font-family: "Montserrat", sans-serif;
      color: #1d1d1d;
      background: transparent;
      border: 0;
      margin: 0;
      padding-left: 0;
      padding-right: 0;
      &:focus {
        box-shadow: none;
      }
      &:after {
          position: absolute;
          right: 5px;
          top: 15px;
      }
    }
    .dropdown-menu {
      padding: 10px;
      .custom-checkbox {
        display: flex;
        padding: 5px 0;
        input {
          margin-right: 7px;
        }
        label {
          flex: 1 1 0;
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
</style>

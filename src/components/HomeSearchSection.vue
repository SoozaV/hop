<template>
  <b-container class="home-search">
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
                  v-model="selectedDisponibilidad"
                  :options="optionsDisponibilidad"
                ></b-form-select>
              </b-form-group>
            </b-col>
            <b-col class="right-form-col col">
              <b-form-group
                id="input-group-1"
                label="Características"
                label-for="input-1"
                label-align="left"
                class="custom-select"
              >
                <!-- Características -->
                <b-form-select
                  onfocus="this.size=5;"
                  onblur="this.size=1;"
                  onchange="this.size=1; this.blur();"
                  onfocusout="this.size=null;"
                  v-model="selectedCaracteristicas"
                  :options="optionsCaracteristicas"
                ></b-form-select>
              </b-form-group>
            </b-col>
          </b-row>

          <b-row class="form-field-container mt-2 mx-auto">
            <b-col>
              <b-form-group
                id="input-group-1"
                label="Presupuesto"
                label-for="input-1"
                label-align="left"
                class="custom-select"
              >
                <!-- Presupuesto -->
                <b-form-select
                  onfocus="this.size=5;"
                  onblur="this.size=1;"
                  onchange="this.size=1; this.blur();"
                  onfocusout="this.size=null;"
                  v-model="selectedPresupuesto"
                  :options="optionsPresupuesto"
                ></b-form-select>
              </b-form-group>
            </b-col>
            <b-col class="right-form-col col">
              <b-form-group
                id="input-group-1"
                label="Intereses personales"
                label-for="input-1"
                label-align="left"
                class="custom-select"
              >
                <!-- About -->
                <b-form-select
                  onfocus="this.size=5;"
                  onblur="this.size=1;"
                  onchange="this.size=1; this.blur();"
                  onfocusout="this.size=null;"
                  v-model="selectedIntereses"
                  :options="optionsIntereses"
                ></b-form-select>
              </b-form-group>
            </b-col>
          </b-row>
          <b-row>
            <b-col>
              <b-button type="submit" class="hop-btn shadow-none"
                >Búsqueda</b-button
              >
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
      selectedDisponibilidad: null,
      selectedCaracteristicas: null,
      selectedPresupuesto: null,
      selectedIntereses: null,
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
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
.home-search {
  margin: 0;
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
  input {
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
  background-color: #fcca2e!important;
  font-family: "Montserrat", sans-serif;
  border: 0;
  color: #1d1d1d!important;
  font-size: 12px;
  border-radius: 50px;
  margin-top: 39px;
  padding: 9px 33px;
}
</style>

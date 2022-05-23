<template>
  <div>
    <section>
      <HeroRegistro msg="Registra tu espacio en tan sólo unos pasos" />
    </section>
    <section>
      <RegisterFormOne />
    </section>
    <section class="mt-5 form-two">
      <b-container>
        <b-row>
          <b-col lg="4" offset-lg="2" class="mb-5">
            <b-form-group
              id="input-group-espacio"
              label-for="input-espacio"
              label-align="left"
              class="custom-select"
            >
              <b-dropdown size="md" text="Tarifa" boundary="viewport">
                <b-form-checkbox name="checkbox-1"> Opción 1 </b-form-checkbox>
                <b-form-checkbox name="checkbox-2"> Opción 2 </b-form-checkbox>
                <b-form-checkbox name="checkbox-3"> Opción 3 </b-form-checkbox>
              </b-dropdown>
            </b-form-group>
          </b-col>
          <b-col lg="4">
            <b-form-group
              id="input-group-espacio"
              label-for="input-espacio"
              label-align="left"
              class="custom-select"
            >
              <b-dropdown size="md" text="Horario" boundary="viewport">
                <b-form-checkbox name="checkbox-1"> Opción 1 </b-form-checkbox>
                <b-form-checkbox name="checkbox-2"> Opción 2 </b-form-checkbox>
                <b-form-checkbox name="checkbox-3"> Opción 3 </b-form-checkbox>
              </b-dropdown>
            </b-form-group>
          </b-col>
        </b-row>
        <b-row class="mt-5 mb-5">
          <b-col lg="4" offset-lg="2" class="mb-5">
            <div class="d-flex justify-content-between">
              <label for="form-capacidad">Capacidad</label>
              <b-form-spinbutton
                id="form-capacidad"
                min="1"
                max="100"
              ></b-form-spinbutton>
            </div>
          </b-col>
          <b-col lg="4">
            <div class="d-flex justify-content-between">
              <label for="form-capacidad">Metros cuadrados</label>
              <b-form-spinbutton
                id="form-metros-cuadrados"
                min="1"
                max="100"
              ></b-form-spinbutton>
            </div>
          </b-col>
        </b-row>
      </b-container>
    </section>
    <section class="section">
      <b-container class="custom-check-section">
        <b-row>
          <b-col cols="12" lg="8" class="col" style="margin: 0 auto !important">
            <h2 class="mt-3 mb-4" style="text-align: center">
              ¿Cuál de estas opciones describe mejor tu espacio?
            </h2>
          </b-col>
        </b-row>
        <b-row>
          <b-col class="mb-3" lg="3" sm="6" cols="6">
            <b-form-checkbox>Cafetería</b-form-checkbox>
          </b-col>
          <b-col class="mb-3" lg="3" sm="6" cols="6">
            <b-form-checkbox>Co Working</b-form-checkbox>
          </b-col>
          <b-col class="mb-3" lg="3" sm="6" cols="6">
            <b-form-checkbox>Co Living</b-form-checkbox>
          </b-col>
          <b-col class="mb-3" lg="3" sm="6" cols="6">
            <b-form-checkbox>Home Office</b-form-checkbox>
          </b-col>
        </b-row>
        <b-row>
          <b-col class="mb-3" lg="3" sm="6" cols="6">
            <b-form-checkbox>Cafetería</b-form-checkbox>
          </b-col>
          <b-col class="mb-3" lg="3" sm="6" cols="6">
            <b-form-checkbox>Co Working</b-form-checkbox>
          </b-col>
          <b-col class="mb-3" lg="3" sm="6" cols="6">
            <b-form-checkbox>Co Living</b-form-checkbox>
          </b-col>
          <b-col class="mb-3" lg="3" sm="6" cols="6">
            <b-form-checkbox>Home Office</b-form-checkbox>
          </b-col>
        </b-row>
      </b-container>
    </section>
    <section class="section">
      <b-container class="custom-check-section">
        <b-row>
          <b-col cols="12" lg="8" class="col" style="margin: 0 auto !important">
            <h2 class="mt-3 mb-4" style="text-align: center">
              ¿Qué tipo de área de trabajo vas a compartir?
            </h2>
          </b-col>
        </b-row>
        <b-row>
          <b-col class="mb-3" lg="3" sm="6" cols="6">
            <b-form-checkbox>Escritorio compartido</b-form-checkbox>
          </b-col>
          <b-col class="mb-3" lg="3" sm="6" cols="6">
            <b-form-checkbox>Escritorio Personal</b-form-checkbox>
          </b-col>
          <b-col class="mb-3" lg="3" sm="6" cols="6">
            <b-form-checkbox>Oficina privada</b-form-checkbox>
          </b-col>
          <b-col class="mb-3" lg="3" sm="6" cols="6">
            <b-form-checkbox>Sala de reuniones</b-form-checkbox>
          </b-col>
        </b-row>
      </b-container>
    </section>
    <section class="section">
      <b-container class="custom-check-section">
        <b-row>
          <b-col cols="12" lg="8" class="col" style="margin: 0 auto !important">
            <h2 class="mt-3 mb-4" style="text-align: center">
              ¿Cómo el ambiente en tu espacio?
            </h2>
          </b-col>
        </b-row>
        <b-row>
          <b-col class="mb-3" lg="3" sm="6" cols="6">
            <b-form-checkbox>Amigable</b-form-checkbox>
          </b-col>
          <b-col class="mb-3" lg="3" sm="6" cols="6">
            <b-form-checkbox>Colaborativo</b-form-checkbox>
          </b-col>
          <b-col class="mb-3" lg="3" sm="6" cols="6">
            <b-form-checkbox>Espacios cómodos</b-form-checkbox>
          </b-col>
          <b-col class="mb-3" lg="3" sm="6" cols="6">
            <b-form-checkbox>Limpio / ordenado</b-form-checkbox>
          </b-col>
        </b-row>
        <b-row>
          <b-col class="mb-3" lg="3" sm="6" cols="6">
            <b-form-checkbox>Social / Networking</b-form-checkbox>
          </b-col>
          <b-col class="mb-3" lg="3" sm="6" cols="6">
            <b-form-checkbox>Silencioso</b-form-checkbox>
          </b-col>
          <b-col class="mb-3" lg="3" sm="6" cols="6">
            <b-form-checkbox>EJEMPLO</b-form-checkbox>
          </b-col>
          <b-col class="mb-3" lg="3" sm="6" cols="6">
            <b-form-checkbox>Limpio / ordenado</b-form-checkbox>
          </b-col>
        </b-row>
      </b-container>
    </section>
    <section class="section">
      <b-container class="custom-check-section img">
        <b-row>
          <b-col cols="12" lg="8" class="col" style="margin: 0 auto !important">
            <h2 class="mt-3 mb-4" style="text-align: center">
              ¿Con que tipo de áreas comunes cuenta?
            </h2>
          </b-col>
        </b-row>
        <b-row>
          <b-col class="mb-3" lg="3" sm="6" cols="6">
            <b-form-checkbox style="flex-direction: column">
              <div class="img-btn">
                <img :src="require('../assets/img/pool@2x.png')" />
                <span>Amigable</span>
              </div>
            </b-form-checkbox>
          </b-col>
          <b-col class="mb-3" lg="3" sm="6" cols="6">
            <b-form-checkbox>
              <div class="img-btn">
                <img :src="require('../assets/img/sunbathing@2x.png')" />
                <span>Área de descanso</span>
              </div>
            </b-form-checkbox>
          </b-col>
          <b-col class="mb-3" lg="3" sm="6" cols="6">
            <b-form-checkbox>
              <div class="img-btn">
                <img :src="require('../assets/img/yoga@2x.png')" />
                <span>Área de meditación</span>
              </div>
            </b-form-checkbox>
          </b-col>
          <b-col class="mb-3" lg="3" sm="6" cols="6">
            <b-form-checkbox>
              <div class="img-btn">
                <img :src="require('../assets/img/barbecue@2x.png')" />
                <span>Asador</span>
              </div>
            </b-form-checkbox>
          </b-col>
        </b-row>
        <b-row>
          <b-col class="mb-3" lg="3" sm="6" cols="6">
            <b-form-checkbox>
              <div class="img-btn">
                <img :src="require('../assets/img/kitchen@2x.png')" />
                <span>Cocina</span>
              </div>
            </b-form-checkbox>
          </b-col>
          <b-col class="mb-3" lg="3" sm="6" cols="6">
            <b-form-checkbox>
              <div class="img-btn">
                <img :src="require('../assets/img/comedor@2x.png')" />
                <span>Comedor</span>
              </div>
            </b-form-checkbox>
          </b-col>
          <b-col class="mb-3" lg="3" sm="6" cols="6">
            <b-form-checkbox>
              <div class="img-btn">
                <img :src="require('../assets/img/jardin@2x.png')" />
                <span>Jardín</span>
              </div>
            </b-form-checkbox>
          </b-col>
          <b-col class="mb-3" lg="3" sm="6" cols="6">
            <b-form-checkbox>
              <div class="img-btn">
                <img :src="require('../assets/img/book@2x.png')" />
                <span>Biblioteca</span>
              </div>
            </b-form-checkbox>
          </b-col>
        </b-row>
        <b-row>
          <b-col class="mb-3" lg="3" sm="6" cols="6">
            <b-form-checkbox>
              <div class="img-btn">
                <img :src="require('../assets/img/desktop@2x.png')" />
                <span>Mesa de Trabajo</span>
              </div>
            </b-form-checkbox>
          </b-col>
          <b-col class="mb-3" lg="3" sm="6" cols="6">
            <b-form-checkbox>
              <div class="img-btn">
                <img :src="require('../assets/img/game@2x.png')" />
                <span>Sala de juegos</span>
              </div>
            </b-form-checkbox>
          </b-col>
          <b-col class="mb-3" lg="3" sm="6" cols="6">
            <b-form-checkbox>
              <div class="img-btn">
                <img :src="require('../assets/img/roof@2x.png')" />
                <span>Roof</span>
              </div>
            </b-form-checkbox>
          </b-col>
          <b-col class="mb-3" lg="3" sm="6" cols="6">
            <b-form-checkbox>
              <div class="img-btn">
                <img :src="require('../assets/img/read@2x.png')" />
                <span>Zona De lectura</span>
              </div>
            </b-form-checkbox>
          </b-col>
        </b-row>
      </b-container>
    </section>
    <section class="section">
      <b-container class="custom-check-section">
        <b-row>
          <b-col cols="12" lg="8" class="col" style="margin: 0 auto !important">
            <h2 class="mt-3 mb-4" style="text-align: center">
              Servicios incluidos
            </h2>
          </b-col>
        </b-row>
        <b-row>
          <b-col class="mb-3" lg="2" sm="6" cols="6">
            <b-form-checkbox>Agua potable</b-form-checkbox>
          </b-col>
          <b-col class="mb-3" lg="2" sm="6" cols="6">
            <b-form-checkbox>Aire<br />acondicionado</b-form-checkbox>
          </b-col>
          <b-col class="mb-3" lg="2" sm="6" cols="6">
            <b-form-checkbox>Cabina Telefónica</b-form-checkbox>
          </b-col>
          <b-col class="mb-3" lg="2" sm="6" cols="6">
            <b-form-checkbox>Café & Té</b-form-checkbox>
          </b-col>
          <b-col class="mb-3" lg="2" sm="6" cols="6">
            <b-form-checkbox>Calefacción</b-form-checkbox>
          </b-col>
          <b-col class="mb-3" lg="2" sm="6" cols="6">
            <b-form-checkbox>Cerveza</b-form-checkbox>
          </b-col>
        </b-row>
        <b-row>
          <b-col class="mb-3" lg="2" sm="6" cols="6">
            <b-form-checkbox>Circuito cerrado </b-form-checkbox>
          </b-col>
          <b-col class="mb-3" lg="2" sm="6" cols="6">
            <b-form-checkbox>Enchufes cargadores</b-form-checkbox>
          </b-col>
          <b-col class="mb-3" lg="2" sm="6" cols="6">
            <b-form-checkbox>Estacionamiento</b-form-checkbox>
          </b-col>
          <b-col class="mb-3" lg="2" sm="6" cols="6">
            <b-form-checkbox>Lockers</b-form-checkbox>
          </b-col>
          <b-col class="mb-3" lg="2" sm="6" cols="6">
            <b-form-checkbox>Proyector</b-form-checkbox>
          </b-col>
          <b-col class="mb-3" lg="2" sm="6" cols="6">
            <b-form-checkbox>Portero</b-form-checkbox>
          </b-col>
        </b-row>
        <b-row>
          <b-col class="mb-3" lg="2" sm="6" cols="6">
            <b-form-checkbox>Sala de juntas</b-form-checkbox>
          </b-col>
          <b-col class="mb-3" lg="2" sm="6" cols="6">
            <b-form-checkbox>Servicios<br />Agua-Luz-Gas</b-form-checkbox>
          </b-col>
          <b-col class="mb-3" lg="2" sm="6" cols="6">
            <b-form-checkbox>Seguridad Privada</b-form-checkbox>
          </b-col>
          <b-col class="mb-3" lg="2" sm="6" cols="6">
            <b-form-checkbox>WC</b-form-checkbox>
          </b-col>
          <b-col class="mb-3" lg="2" sm="6" cols="6">
            <b-form-checkbox>Silla cómoda</b-form-checkbox>
          </b-col>
          <b-col class="mb-3" lg="2" sm="6" cols="6">
            <b-form-checkbox>Wifi</b-form-checkbox>
          </b-col>
        </b-row>
      </b-container>
    </section>
    <section class="section">
      <b-container class="custom-check-section">
        <b-row>
          <b-col cols="12" lg="8" class="col" style="margin: 0 auto !important">
            <h2 class="mt-3 mb-4" style="text-align: center">
              Servicios extra (No incluidos en el costo)
            </h2>
          </b-col>
        </b-row>
        <b-row class="justify-content-center">
          <b-col class="mb-3" lg="2" sm="6" cols="6">
            <b-form-checkbox>Agua potable</b-form-checkbox>
          </b-col>
          <b-col class="mb-3" lg="2" sm="6" cols="6">
            <b-form-checkbox>Aire<br />acondicionado</b-form-checkbox>
          </b-col>
          <b-col class="mb-3" lg="2" sm="6" cols="6">
            <b-form-checkbox>Cabina Telefónica</b-form-checkbox>
          </b-col>
          <b-col class="mb-3" lg="2" sm="6" cols="6">
            <b-form-checkbox>Café & Té</b-form-checkbox>
          </b-col>
          <b-col class="mb-3" lg="2" sm="6" cols="6">
            <b-form-checkbox>Calefacción</b-form-checkbox>
          </b-col>
        </b-row>
        <b-row class="justify-content-center">
          <b-col class="mb-3" lg="2" sm="6" cols="6">
            <b-form-checkbox>Circuito cerrado </b-form-checkbox>
          </b-col>
          <b-col class="mb-3" lg="2" sm="6" cols="6">
            <b-form-checkbox>Enchufes cargadores</b-form-checkbox>
          </b-col>
          <b-col class="mb-3" lg="2" sm="6" cols="6">
            <b-form-checkbox>Estacionamiento</b-form-checkbox>
          </b-col>
          <b-col class="mb-3" lg="2" sm="6" cols="6">
            <b-form-checkbox>Lockers</b-form-checkbox>
          </b-col>
          <b-col class="mb-3" lg="2" sm="6" cols="6">
            <b-form-checkbox>Proyector</b-form-checkbox>
          </b-col>
        </b-row>
      </b-container>
    </section>
    <section class="section">
      <b-container class="custom-check-section">
        <b-row>
          <b-col cols="12" lg="8" class="col" style="margin: 0 auto !important">
            <h2 class="mt-3 mb-4" style="text-align: center">Reglas</h2>
          </b-col>
        </b-row>
        <b-row class="justify-content-center">
          <b-col class="mb-3" lg="2" sm="6" cols="6">
            <b-form-checkbox>Eco-Friendly</b-form-checkbox>
          </b-col>
          <b-col class="mb-3" lg="2" sm="6" cols="6">
            <b-form-checkbox>Fumar sólo en áreas permitidas</b-form-checkbox>
          </b-col>
          <b-col class="mb-3" lg="2" sm="6" cols="6">
            <b-form-checkbox>No niños</b-form-checkbox>
          </b-col>
          <b-col class="mb-3" lg="2" sm="6" cols="6">
            <b-form-checkbox>No alimentos</b-form-checkbox>
          </b-col>
        </b-row>
        <b-row class="justify-content-center">
          <b-col class="mb-3" lg="2" sm="6" cols="6">
            <b-form-checkbox>No invitados</b-form-checkbox>
          </b-col>
          <b-col class="mb-3" lg="2" sm="6" cols="6">
            <b-form-checkbox>No ruido</b-form-checkbox>
          </b-col>
          <b-col class="mb-3" lg="2" sm="6" cols="6">
            <b-form-checkbox>No mascotas</b-form-checkbox>
          </b-col>
          <b-col class="mb-3" lg="2" sm="6" cols="6">
            <b-form-checkbox>Pet-Friendly</b-form-checkbox>
          </b-col>
        </b-row>
      </b-container>
    </section>
    <section>
      <b-container>
        <b-row class="mt-5">
          <b-col>
            <div
              class="dragNdrop"
              style="border: 1px solid; border-radius: 15px;"
              @dragover.prevent
              @drop.prevent
            >
              <div @drop="dragFile" style="margin-bottom: 10px; padding: 10px">
                <img :src="require('../assets/img/photos@2x.png')" />
                <b-form-file
                  style="display: none"
                  multiple
                  @change="uploadFile"
                  accept="image/jpeg, image/png, image/gif"
                ></b-form-file>
                <h2>Arrastra las fotos aquí</h2>
                <h3>Agrega por lo menos 5 fotos</h3>
                <div v-if="File.length">
                  <ul v-for="file in File" :key="file">
                    <li>{{ file.name }}</li>
                  </ul>
                </div>

                <label
                  >Sube fotos desde tu dispositivo
                  <b-form-file
                    style="display: none"
                    multiple
                    @change="uploadFile"
                    accept="image/jpeg, image/png, image/gif"
                  ></b-form-file>
                </label>
              </div>
            </div>
          </b-col>
        </b-row>
        <b-row>
            <b-col>
              <b-button
                type="submit"
                class="hop-btn shadow-none"
                style="margin-right: 5px"
              >
                Registrar
              </b-button>
            </b-col>
          </b-row>
      </b-container>
    </section>
    <Footer />
  </div>
</template>

<script>
// @ is an alias to /src
import HeroRegistro from "@/components/HeroRegistro.vue";
import RegisterFormOne from "@/components/RegisterFormOne.vue";
import CTABanner from "@/components/CTABanner.vue";
import NearYou from "@/components/NearYou.vue";
import Footer from "@/components/Footer.vue";

export default {
  name: "Home",
  components: {
    HeroRegistro,
    RegisterFormOne,
    CTABanner,
    NearYou,
    Footer,
  },
  data() {
    return {
      File: [],
    };
  },
  methods: {
    uploadFile(e) {
      this.File = e.target.files;
    },
    dragFile(e) {
      this.File = e.dataTransfer.files;
    },
  },
};
</script>

<style lang="scss">
.section {
  .custom-check-section {
    &.img {
      .custom-checkbox {
        label {
          height: inherit;
          padding-top: 10px;
          padding-bottom: 10px;
        }
      }
    }
    .custom-checkbox {
      label {
        background: #e6e6e6;
        font-family: "Montserrat", sans-serif;
        color: #1d1d1d;
        font-weight: bold;
        height: 100px;
        border-radius: 15px;
        display: flex;
        justify-content: center;
        align-items: center;
        div.img-btn {
          display: flex;
          flex-direction: column;
          align-items: center;
          img {
            max-width: 90px;
          }
        }
      }
      input {
        display: none;
        &:checked + label {
          background: #fcca2e;
        }
      }
    }
  }
  h2 {
    font-family: "Montserrat", sans-serif;
    color: #1d1d1d;
    font-weight: 800;
    font-size: 20px;
  }
}
.form-two {
  .b-form-spinbutton {
    width: 120px;
    border: 0;
    &:focus,
    &:focus-visible {
      box-shadow: none;
    }
    button {
      &:first-child,
      &:last-child {
        background: #fcca2e;
        color: #1d1d1d;
        border-radius: 100px !important;
        width: 24px;
        display: flex;
        justify-content: center;
        align-items: center;
      }
    }
  }
  .b-dropdown {
    width: 100%;
    button.btn {
      text-align: left;
      font-family: "Montserrat", sans-serif;
      color: #1d1d1d;
      background: transparent;
      border: 0;
      border-bottom: 1px solid #b5b5b5;
      margin: 0;
      border-radius: 0;
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
        align-items: center;
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
}
.dragNdrop {
  h2 {
    margin-top: 30px;
    font-family: "Montserrat", sans-serif;
    color: #1d1d1d;
    font-weight: bold;
    font-size: 24px;
  }
  h3 {
    font-family: "Montserrat", sans-serif;
    color: #b5b5b5;
    font-weight: 400;
    font-size: 18px;
  }
  label {
    font-family: "Montserrat", sans-serif;
    color: #1d1d1d;
    font-weight: bold;
    font-size: 12px;
    text-decoration: underline;
  }
}
</style>

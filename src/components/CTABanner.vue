<template>
  <b-container>
    <b-row>
      <b-col>
        <b-row class="cta-section">
          <b-col>
            <h2>Conviértete en Anfitrión</h2>
            <h3>
              Comparte o promociona tu espacio de trabajo y genera ingresos
              extra.
            </h3>
            <b-button to="/registro" type="submit" class="hop-btn shadow-none"
              >Regístrate</b-button
            >
          </b-col>
        </b-row>
        <b-row style="max-width: 620px!important; margin: 0 auto;">
          <b-col style="padding-left: 0; padding-right: 0;">
            <b-img :src="ctaBackground" fluid-grow alt="" style="margin-bottom: 10px; max-width: 100%"></b-img>
          </b-col>
        </b-row>
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
export default {
  name: "CTABanner",
  data() {
    return {
      ctaBackground: require("../assets/img/cta@4x.webp"),
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss">
.cta-section {
  background: #1d1d1d;
  max-width: 620px!important;
  margin: 39px auto 0 !important;
  padding-top: 45px;
  border-radius: 10px 10px 0 0;

  .col {
    h2,
    h3 {
      text-align: center;
      font-family: "Montserrat", sans-serif;
      color: white;
      font-weight: 800;
      font-size: 20px;
    }
    h2 {
      margin-bottom: 11px;
    }
    h3 {
      font-size: 12px;
      font-weight: 400;
      line-height: 1.4em;
    }
    .btn.hop-btn {
      background-color: #fcca2e !important;
      font-family: "Montserrat", sans-serif;
      border: 0;
      color: #1d1d1d !important;
      font-size: 12px;
      border-radius: 50px;
      margin-top: 30px;
      margin-bottom: 35px;
      padding: 9px 33px;
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
</style>

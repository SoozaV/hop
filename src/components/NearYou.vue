<template>
  <b-container class="home-search">
    <b-row>
      <b-col>
        <h2>Cerca de ti</h2>
        <h3>Descubre cientos de opciones que tenemos para ti.</h3>
      </b-col>
    </b-row>
    <b-row>
      <b-col sm="12" md="6" lg="4">
        <Property />
      </b-col>
      <b-col sm="12" md="6" lg="4">
        <Property bgColor="#e3e3e3" />
      </b-col>
      <b-col sm="12" md="6" lg="4">
        <Property />
      </b-col>
      <b-col cols="12">
        <b-button type="submit" class="hop-btn shadow-none"
          >Mostrar más</b-button
        >
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
import Property from "@/components/Property.vue";

export default {
  name: "NearYou",
  components: {
    Property,
  },
  data() {
    return {};
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
  background-color: #fcca2e !important;
  font-family: "Montserrat", sans-serif;
  border: 0;
  color: #1d1d1d !important;
  font-size: 12px;
  font-weight: bold;
  border-radius: 50px;
  margin-top: 39px;
  padding: 9px 33px;
}
</style>

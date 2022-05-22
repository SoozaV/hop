<template>
  <b-container class="map-header">
    <b-row>
      <b-col class="form-field-container"
        ><iframe
          src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d9499.727339573088!2d-96.10459913668147!3d19.109000714288715!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x85c3403415555555%3A0x63711bdd4f42c2f0!2sPlaya%20Boca%20Del%20Rio!5e0!3m2!1ses-419!2smx!4v1653246304517!5m2!1ses-419!2smx"
          width="1920"
          height="450"
          style="border: 0"
          allowfullscreen=""
          loading="lazy"
          referrerpolicy="no-referrer-when-downgrade"
        ></iframe>
        <b-form-group
          class="map-input"
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
  </b-container>
</template>

<script>
export default {
  name: "HeroSection",
  props: {
    msg: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.map-header {
  height: 276px;
  min-width: 100%;
  background: #000; /* fallback colour. Make sure this is just one solid colour. */
  background: -webkit-linear-gradient(rgba(0, 0, 0, 0.6), rgba(0, 0, 0, 0.6)),
    url("../assets/img/Header_Image@4x.webp");
  background: linear-gradient(rgba(0, 0, 0, 0.6), rgba(0, 0, 0, 0.6)),
    url("../assets/img/Header_Image@4x.webp"); /* The least supported option. */
  background-size: cover;
  padding: 0;
  margin: 0;
  overflow: hidden;
  display: flex;
  align-items: center;
  justify-content: center;
}
.map-header .map-input {
  position: absolute;
  z-index: 999999;
  left: 50%;
  top: 50px;
  transform: translateX(-50%) translateY(100%);
  padding: 10px;
  border-radius: 10px;
  border: 1px solid;
  width: 80%;
  background: white;
}
.map-header .form-field-container {
  border: 1px solid #1d1d1d;
  padding: 9px 2px 5px;
  border-radius: 10px;
  max-width: 100%;
}

.map-header .form-field-container input {
  padding: 0;
  border: 0;
  font-family: "Montserrat", sans-serif;
}
.map-header .form-field-container label {
  font-family: "Montserrat", sans-serif;
  font-size: 10px;
  text-transform: uppercase;
  font-weight: bold;
}
.map-header .form-field-container label.text-left {
  text-align: left;
}
.home-header h1 {
  color: white;
  font-weight: bold;
}
.home-header span {
  width: 35px;
  height: 4px;
  background: white;
  display: block;
  margin: 0 auto;
  border-radius: 3px;
}
</style>

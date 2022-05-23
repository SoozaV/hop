<template>
  <b-container class="registro-header">
    <b-row>
      <b-col
        ><h1>{{ msg }}</h1>
        <h4>Únete a la comunidad. Te ayudaremos en cada paso del proceso.</h4>
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
.registro-header {
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
.registro-header h1 {
  color: white;
  font-weight: bold;
}
.registro-header h4 {
  color: white;
  font-weight: 400;
  font-family: "Montserrat", sans-serif;
}
.registro-header span {
  width: 35px;
  height: 4px;
  background: white;
  display: block;
  margin: 0 auto;
  border-radius: 3px;
}
</style>

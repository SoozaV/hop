<template>
  <b-container class="home-header">
    <b-row>
      <b-col
        ><h1>{{ msg }}</h1>
        <span></span>
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
.home-header {
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

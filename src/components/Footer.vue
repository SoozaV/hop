<template>
  <b-container>
    <b-row>
      <b-col>
        <b-row class="footer-section">
          <b-col>
            <p>© 2022 Home Office Partner. All Rights Reserved</p>
            <p>Términos y Condiciones • Newsletter</p>
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
.footer-section {
  border-top: 1px solid #707070;
  max-width: 100%;
  margin: 39px auto 0 !important;
  padding-top: 24px;
 p {
   color: #d0d0d0;
   font-size: 11px;
   font-family: "Montserrat", sans-serif;
   &:first-child {
     margin-bottom: 5px;
   }
 }
  
  
}
</style>

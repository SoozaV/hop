<template>
  <div>
    <section>
      <Map />
    </section>
    <section>
      <HomeAdvancedSearchSection />
    </section>
    <section>
      <CTABanner />
    </section>
    <section>
      <NearYou />
    </section>
    <Footer />
  </div>
</template>

<script>
// @ is an alias to /src
import Map from "@/components/Map.vue";
import HomeAdvancedSearchSection from "@/components/HomeAdvancedSearchSection.vue";
import CTABanner from "@/components/CTABanner.vue";
import NearYou from "@/components/NearYou.vue";
import Footer from "@/components/Footer.vue";

export default {
  name: "Home",
  components: {
    Map,
    HomeAdvancedSearchSection,
    CTABanner,
    NearYou,
    Footer
  },
};
</script>

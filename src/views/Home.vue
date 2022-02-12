<template>
  <div>
    <section>
      <HeroSection msg="Home office partner" />
    </section>
    <section>
      <HomeSearchSection />
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
import HeroSection from "@/components/HeroSection.vue";
import HomeSearchSection from "@/components/HomeSearchSection.vue";
import CTABanner from "@/components/CTABanner.vue";
import NearYou from "@/components/NearYou.vue";
import Footer from "@/components/Footer.vue";

export default {
  name: "Home",
  components: {
    HeroSection,
    HomeSearchSection,
    CTABanner,
    NearYou,
    Footer
  },
};
</script>

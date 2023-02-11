<template>
  <Hero />
  <Features />
  <Pricing />
  <Fuel />
  <Pipeline />
  <Ready />
  <Footer />
</template>

<script>
import Hero from "./components/Hero.vue";
import Features from "./components/Features.vue";
import Pricing from "./components/Pricing.vue";
import Fuel from "./components/Fuel.vue";
import Pipeline from "./components/Pipeline.vue";
import Ready from "./components/Ready.vue";
import Footer from "./components/Footer.vue";
export default {
  name: "App",
  components: {
    Hero,
    Features,
    Pricing,
    Fuel,
    Pipeline,
    Ready,
    Footer,
  },
};
</script>

<style></style>

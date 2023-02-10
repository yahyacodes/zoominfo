<template>
  <Hero />
  <Features />
  <Pricing />
  <Fuel />
  <Pipeline />
</template>

<script>
import Hero from "./components/Hero.vue";
import Features from "./components/Features.vue";
import Pricing from "./components/Pricing.vue";
import Fuel from "./components/Fuel.vue";
import Pipeline from "./components/Pipeline.vue";
export default {
  name: "App",
  components: {
    Hero,
    Features,
    Pricing,
    Fuel,
    Pipeline,
  },
};
</script>

<style></style>

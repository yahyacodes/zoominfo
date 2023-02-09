<template>
  <Hero />
  <Features />
  <Pricing />
</template>

<script>
import Hero from "./components/Hero.vue";
import Features from "./components/Features.vue";
import Pricing from "./components/Pricing.vue";
export default {
  name: "App",
  components: {
    Hero,
    Features,
    Pricing,
  },
};
</script>

<style></style>

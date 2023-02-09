<template>
  <section class="hero-bg py-28">
    <div>
      <Navbar />
    </div>
    <div class="container text-center">
      <h1 class="font-bold text-4xl text-white header-tag leading-none">
        It's Our Business to Grow Yours<span class="text-red-700">.</span>
      </h1>

      <p class="text-white text-2xl mt-2">
        Get the B2B data and software you need to connect with and close your
        most valuable buyers - all in one operating system.
      </p>

      <form class="flex items-center mx-44 mt-10">
        <div class="relative w-8/12">
          <input
            type="email"
            class="bg-gray-50 border border-red-600 text-gray-900 text-base rounded-full focus:ring-none focus:border-none w-full py-3 px-2"
            placeholder="Business Email"
            required
          />
        </div>
        <button
          type="submit"
          class="py-3 px-10 text-base font-medium text-white bg-red-700 rounded-full border-none mx-2"
        >
          Free Trial
        </button>
      </form>
      <span class="text-xs text-white">
        By submitting this form,you are agreeing to Zoominfo's
        <span class="underline">Privacy Policy</span> and
        <span class="underline">Terms of Services</span>
      </span>

      <div class="mt-32 text-center">
        <h1 class="text-white">TRUSTED BY 30,000+ BUSINESSES</h1>
      </div>

      <div class="mx-auto ml-40 flex flex-wrap mt-10">
        <div
          class="w-full text-center md:w-1/2 lg:w-1/2 xl:w-1/4 lg:px-8 mb-20 lg:mb-0"
        >
          <img src="../assets/snowflake-logo-white.png" alt="" />
        </div>

        <div
          class="w-full text-center md:w-1/2 lg:w-1/2 xl:w-1/4 lg:px-8 mb-20 lg:mb-0"
        >
          <img src="../assets/paypal-logo-removebg-preview.png" alt="" />
        </div>

        <div
          class="w-full text-center md:w-1/2 lg:w-1/2 xl:w-1/4 lg:px-8 mb-20 lg:mb-0"
        >
          <img src="../assets/unilever-2-logo-01-01.png" alt="" />
        </div>
      </div>
    </div>
  </section>
</template>
<script>
import Navbar from "./Navbar.vue";
export default {
  name: "Hero",
  components: {
    Navbar,
  },
};
</script>
<style></style>

<template>
  <nav
    class="px-2 bg-white shadow-2xl sm:px-4 py-2.5 fixed w-full z-20 top-0 left-0"
    :class="{ 'sm:bg-transparent sm:shadow-none': !showWhiteBg }"
  >
    <div
      class="container-nav flex flex-wrap items-center justify-between mx-auto"
    >
      <a href="https://flowbite.com/" class="flex items-center">
        <img
          src="../assets/zoominfo-logo-vector.png"
          class="h-6 mr-3 sm:h-9"
          alt="Flowbite Logo"
        />
        <span
          class="self-center text-xl font-semibold whitespace-nowrap"
          :class="{ 'text-white': !showWhiteBg }"
          >zoominfo</span
        >
      </a>
      <div class="flex md:order-2">
        <button
          type="button"
          class="text-white bg-red-700 rounded-full border-none mx-2 font-medium text-sm px-5 py-2.5 text-center mr-3 md:mr-0"
        >
          Get started
        </button>
        <button
          data-collapse-toggle="navbar-sticky"
          type="button"
          class="inline-flex items-center p-2 text-sm text-gray-500 rounded-lg md:hidden"
          aria-controls="navbar-sticky"
          aria-expanded="false"
        >
          <span class="sr-only">Open main menu</span>
          <svg
            class="w-6 h-6"
            aria-hidden="true"
            fill="currentColor"
            viewBox="0 0 20 20"
            xmlns="http://www.w3.org/2000/svg"
          >
            <path
              fill-rule="evenodd"
              d="M3 5a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 10a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1zM3 15a1 1 0 011-1h12a1 1 0 110 2H4a1 1 0 01-1-1z"
              clip-rule="evenodd"
            ></path>
          </svg>
        </button>
      </div>

      <div
        class="items-center justify-between hidden w-full md:flex md:w-auto md:order-1"
        id="navbar-sticky"
      >
        <ul
          class="flex flex-col p-4 mt-4 border rounded-lg md:flex-row md:space-x-8 md:mt-0 md:text-sm md:font-medium md:border-0"
        >
          <li
            class="group relative px-4 text-white cursor-pointer"
            :class="{ 'text-white': !showWhiteBg }"
          >
            Solutions
            <fa icon="chevron-down" class="h-2 mx-2" />
            <div
              class="group-hover:block absolute hidden top-8 bg-white shadow p-5 rounded-2xl"
            >
              <div class="w-full md:w-1/2 2xl:w-1/2 lg:w-1/2 px-3 mb-6">
                <div class="p-8 bg-white rounded-2xl border border-gray-300">
                  <ul class="w-48">
                    <li>
                      <a
                        class="block text-purple-500 font-bold text-base uppercase hover:text-purple-700 cursor-pointer"
                        >Item</a
                      >
                    </li>
                    <li>
                      <a
                        class="block text-purple-500 font-bold text-base uppercase hover:text-purple-700 cursor-pointer"
                        >Item 2</a
                      >
                    </li>
                    <li>
                      <a
                        class="block text-purple-500 font-bold text-base uppercase hover:text-purple-700 cursor-pointer"
                        >Item 3</a
                      >
                    </li>
                    <li>
                      <a
                        class="block text-purple-500 font-bold text-base uppercase hover:text-purple-700 cursor-pointer"
                        >Item 4</a
                      >
                    </li>
                    <li>
                      <a
                        class="block text-purple-500 font-bold text-base uppercase hover:text-purple-700 cursor-pointer"
                        >Item 5</a
                      >
                    </li>
                  </ul>
                </div>
              </div>
            </div>
          </li>
          <li>
            <a
              href="#"
              class="block py-2 pl-3 pr-4 md:p-0"
              :class="{ 'text-white': !showWhiteBg }"
              >Plaform
              <fa icon="chevron-down" class="h-2 mx-2" />
            </a>
          </li>
          <li>
            <a
              href="#"
              class="block py-2 pl-3 pr-4 md:p-0"
              :class="{ 'text-white': !showWhiteBg }"
              >Pricing</a
            >
          </li>
          <li>
            <a
              href="#"
              class="block py-2 pl-3 pr-4 md:p-0"
              :class="{ 'text-white': !showWhiteBg }"
              >Our Data</a
            >
          </li>
          <li>
            <a
              href="#"
              class="block py-2 pl-3 pr-4 md:p-0"
              :class="{ 'text-white': !showWhiteBg }"
              >Resources
              <fa icon="chevron-down" class="h-2 mx-2" />
            </a>
          </li>
        </ul>
      </div>
    </div>
  </nav>
</template>
<script>
import { ref } from "vue";
export default {
  setup() {
    let showWhiteBg = ref(false);

    document.addEventListener("scroll", function () {
      let bodyTopPositon = document.body.getBoundingClientRect().top;

      if (bodyTopPositon < -158) {
        showWhiteBg.value = true;
      } else {
        showWhiteBg.value = false;
      }
    });

    return {
      showWhiteBg,
    };
  },
};
</script>
<style></style>

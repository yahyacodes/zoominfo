<template>
  <nav
    :class="{ scrolled: !view.atTopOfPage }"
    class="px-2 sm:px-4 py-2.5 fixed w-full z-20 top-0 left-0"
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
          class="self-center text-xl text-white font-semibold whitespace-nowrap"
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
          <li>
            <a
              href="#"
              class="block py-2 pl-3 pr-4 text-white md:p-0 nav"
              aria-current="page"
              >Solutions
              <fa icon="chevron-down" class="h-2 mx-2" />
            </a>
          </li>
          <li>
            <a href="#" class="block py-2 pl-3 pr-4 text-white rounded md:p-0"
              >Plaform
              <fa icon="chevron-down" class="h-2 mx-2" />
            </a>
          </li>
          <li>
            <a href="#" class="block py-2 pl-3 pr-4 text-white rounded md:p-0"
              >Pricing</a
            >
          </li>
          <li>
            <a href="#" class="block py-2 pl-3 pr-4 text-white rounded md:p-0"
              >Our Data</a
            >
          </li>
          <li>
            <a href="#" class="block py-2 pl-3 pr-4 text-white rounded md:p-0"
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
export default {
  // in data, I like to store a view object with all
  // the values I need for a component to manage
  // it's 'view' state - ie loading,
  // or in this case, if the user is at the top of the page or not
  data() {
    return {
      view: {
        atTopOfPage: true,
      },
    };
  },

  // a beforeMount call to add a listener to the window
  beforeMount() {
    window.addEventListener("scroll", this.handleScroll);
  },

  methods: {
    // the function to call when the user scrolls, added as a method
    handleScroll() {
      // when the user scrolls, check the pageYOffset
      if (window.pageYOffset > 0) {
        // user is scrolled
        if (this.view.atTopOfPage) this.view.atTopOfPage = false;
      } else {
        // user is at top of page
        if (!this.view.atTopOfPage) this.view.atTopOfPage = true;
      }
    },
  },
};
</script>
<style></style>

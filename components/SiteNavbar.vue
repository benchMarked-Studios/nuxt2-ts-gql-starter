<template>
  <header>
    <div class="antialiased">
      <nav
        class="flex items-center justify-between flex-wrap bg-teal p-6 md:p-20"
      >
        <div class="flex items-center flex-no-shrink text-white mr-6">
          <NuxtLink to="/">
            <img
              class="menu-image"
              src="~assets/images/logo.png"
              width="78px"
              height="58px"
            />
          </NuxtLink>
        </div>
        <div class="block sm:hidden">
          <button
            class="flex items-center px-3 py-2 border rounded text-teal-lighter border-teal-light hover:text-white hover:border-white"
            @click="open = !open"
          >
            <svg
              class="fill-current h-3 w-3"
              viewBox="0 0 20 20"
              xmlns="http://www.w3.org/2000/svg"
            >
              <title>Menu</title>
              <path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z" />
            </svg>
          </button>
        </div>
        <div
          :class="open ? 'block:' : 'hidden'"
          class="w-full flex-grow sm:flex sm:items-center sm:w-auto"
        >
          <div class="text-sm sm:flex-grow">
            <!-- <NuxtLink
              to="/about"
              class="text-2xl font-cursive menu-item no-underline block mt-4 sm:inline-block sm:mt-0 text-teal-lighter hover:text-white mr-4"
            >
              About
            </NuxtLink> -->
            <NuxtLink
              class="text-2xl font-cursive menu-item no-underline block mt-4 sm:inline-block sm:mt-0 text-teal-lighter hover:text-white mr-4"
              to="/blog"
            >
              Blog
            </NuxtLink>
            <a
              class="text-2xl font-cursive menu-item no-underline block mt-4 sm:inline-block sm:mt-0 text-teal-lighter hover:text-white mr-4"
              href="https://status.kavinjey.xyz"
            >
              Status
            </a>
          </div>
          <!-- <div>
            <NuxtLink
              to="/contact"
              class="inline-flex p-3 w-auto text-2xl font-cursive menu-item no-underline border rounded text-black bg-white hover:border-transparent hover:text-teal hover:bg-white mt-4 sm:mt-0"
            >
              Contact
            </NuxtLink>
          </div> -->
        </div>
      </nav>
    </div>
  </header>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  name: 'SiteNavbar',
  data: () => ({
    open: false,
  }),
  methods: {
    toggle() {
      this.open = !this.open
    },
  },
})
</script>

<style>
.menu-image:hover {
  transform: scale(1.25);
  transition: transform 0.5s linear;
}

.menu-item {
  line-height: 150%;
  font-family: 'Rakkas', serif;
  font-weight: 400;
  letter-spacing: 0.025em;
}

.menu-item:hover {
  color: #3ce7db;
  text-decoration: underline;
}
</style>

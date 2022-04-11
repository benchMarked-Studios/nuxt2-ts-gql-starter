<template>
  <footer class="min-h-full footer-2 bg-gray-800 pt-6 md:pt-12">
    <div class="container px-4 mx-auto">
      <div class="md:flex md:flex-wrap md:-mx-4 py-6 md:pb-12">
        <div class="footer-info lg:w-1/3 md:px-4">
          <h4 class="text-white text-2xl mb-4">
            Kavin Jey &#183; Full Stack Developer
          </h4>
          <p class="text-gray-400">Gotta always be learning</p>
        </div>

        <div class="md:w-2/3 lg:w-1/3 md:px-4 xl:pl-16 mt-12 lg:mt-0">
          <div class="sm:flex">
            <div class="sm:flex-1">
              <h6 class="text-base font-medium text-white uppercase mb-2">
                Pages
              </h6>
              <div>
                <NuxtLink
                  to="/about"
                  class="text-gray-400 py-1 block hover:underline"
                >
                  About
                </NuxtLink>
                <NuxtLink
                  to="/blog"
                  class="text-gray-400 py-1 block hover:underline"
                >
                  Blog
                </NuxtLink>
                <NuxtLink
                  to="/contact"
                  class="text-gray-400 py-1 block hover:underline"
                >
                  Contact
                </NuxtLink>
              </div>
            </div>
            <div class="sm:flex-1 mt-4 sm:mt-0">
              <h6 class="text-base font-medium text-white uppercase mb-2">
                Related
              </h6>
              <div>
                <a href="#" class="text-gray-400 py-1 block hover:underline"
                  >Polywork</a
                >
                <a href="#" class="text-gray-400 py-1 block hover:underline"
                  >Twitter</a
                >
                <a href="#" class="text-gray-400 py-1 block hover:underline"
                  >BMS</a
                >
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </footer>
</template>

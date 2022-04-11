<template>
  <div>
    <div class="grid grid-cols-1 grid-rows-1">
      <div class="grid mx-6 md:mx-24 row-span-1 col-span-1 z-10">
        <h1 class="text-6xl text-display">Kavin Jey</h1>
        <p class="text-3xl text-sans mb-10">Full Stack Developer</p>
        <br />

        <p class="text-xl text-sans text-left mb-10 md:w-1/3">
          I&apos;m Kavin. I am a Full Stack Developer with experience working in
          startup and corporate environments, mainly in Javascript and Python
          environments.
        </p>
      </div>
    </div>
    <div
      class="grid max-w-xs md:mx-12 md:-mt-96 row-span-1 col-span-1 place-content-center z-0"
    >
      <!-- <img src="~assets/images/people-typing-codes.png"> -->
      <DeskGraphic />
    </div>

    <div class="space-x-8 my-10 px-10 flex">
      <div class="w-full">
        <h1 class="text-5xl text-orange mb-5">Experience</h1>
        <div class="bg-orange rounded-md shadow-xl p-4">
          <p>Hi There</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>
import Vue from 'vue'
export default Vue.extend({
  name: 'IndexPage',
  layout: 'defaultLayout',
})
</script>

<style>
h1,
h2,
h3,
h4,
h5,
h6,
p {
  text-shadow: 1px 1px 3px rgb(0 0 0 / 29%), 2px 4px 7px rgb(73 64 125 / 35%);
}

.title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>

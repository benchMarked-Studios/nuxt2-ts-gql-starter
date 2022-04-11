<template>
  <div
    class="md:w-full md:mb-0 mb-6 flex flex-col justify-center items-center max-w-xs mx-auto"
  >
    <div
      class="border-gray-500 border-1 bg-gray-300 h-56 w-full rounded-lg shadow-md bg-cover bg-no-repeat bg-center"
      :style="'background-image: url(' + coverImage + ')'"
    />

    <div
      class="w-full h-64 bg-white -mt-10 shadow-lg rounded-lg overflow-hidden p-5"
    >
      <div class="header-content inline-flex">
        <div class="title-post text-stroke-sm font-medium">
          {{ title }}
        </div>
      </div>
      <div class="flex flex-col">
        <div class="summary-post text-gray-500 text-base text-justify">
          {{ brief.substr(0, 150) }}...
          <NuxtLink
            :to="'/blog/' + slug"
            class="bg-blue-100 text-blue-500 px-2 mt-4 block rounded p-2 text-sm"
          >
            <span class>Read More</span>
          </NuxtLink>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'BlogArticle',
  props: {
    slug: String,
    title: String,
    brief: String,
    contentMarkdown: String,
    coverImage: String,
  },
}
</script>

<style scoped>
.category-title,
.summary-post,
.title-post {
  color: rgba(0, 0, 0, 0.75);
}
</style>

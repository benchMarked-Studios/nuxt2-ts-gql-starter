<template>
  <div class="h-screen">
    <div class="flex">
      <h1 class="font-display text-3xl self-center p-4 text-white">title</h1>

      <div class="mx-4 flex flex-wrap space-x-2">
        <a
          class="border-1 bg-orange rounded-3xl text-2xl flex text-center justify-center items-center p-3"
          :href="'https://blog.kavinjey.xyz/' + slug"
          >View on Hashnode<br />
          (looks better here i promise)
        </a>
      </div>
    </div>

    <div class="mx-auto p-4" />
  </div>
</template>

<script lang="ts" setup>
import Vue from 'vue'

export default Vue.extend({
  name: 'ArticleDetailBySlug',
  layout: 'defaultLayout',
  asyncData({ params }) {
    const slug = params.slug
    return {
      slug,
      data: {
        post: {
          title: 'ur nan',
          content: '<p> hello </p>',
          slug: 'teststs',
        },
      },
    }
  },
})
</script>

<template>
  <div>
    <div class="flex mx-auto p-4 mx-24">
      <h1 class="text-left text-6xl text-display sm:m-10 p-4">Articles</h1>
      <!-- <p class="text-xl text-sans">
        Collection of writing
      </p> -->
    </div>
    <div class="container mr-auto py-4">
      <div class="flex flex-wrap">
        <!-- <div  
          v-if="articles"
          >
            <Article        
              v-for="(entry, i) of articles?.user.publication.posts"
              :key="i"
              :cover-image="entry.coverImage"
              :slug="entry.slug"
              :title="entry.title"
              :brief="entry.brief"
              :content-markdown="entry.contentMarkdown"
            />
          </div> -->
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>
import Vue from 'vue'

export default Vue.extend({
  name: 'BlogPage',
  layout: 'defaultLayout',
})

// const { data, pending } = await useAsyncData('articles', () => GqlArticles())
</script>

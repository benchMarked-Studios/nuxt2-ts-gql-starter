<template>
  <div>
    <div class="container">
      <button class="btn">Click Me</button>
      <div class="card">
        <button class="btn">Click Me</button>
      </div>
      <div class="card">
        <p class="body">Here is some text</p>
        <h1 class="title">Here is some text</h1>
        <h2 class="subtitle">Here is some text</h2>
      </div>
    </div>
    <div class="md:mx-24 flex">
      <div class="flex flex-col mx-4">
        <h1 class="text-6xl text-display">Kavin Jey</h1>
        <p class="text-3xl text-sans mb-10">Full Stack Developer</p>
        <br />

        <p class="text-xl text-sans text-left mb-10">
          Hi there! I&apos;m Kavin.
          <br />
          I am a Full Stack Developer with experience working in startup and
          corporate environments, mainly in Javascript and Python environments.
        </p>
        <p class="text-xl text-sans text-right mb-10">
          This site is a constant work-in-progress.
          <br />
          I use this space to write out technical articles, <br />
          try out new tech, as well as display some of the projects I've worked
          on.
        </p>
      </div>

      <Mosaic />
    </div>
    <div class="flex">
      <!-- <img src="~assets/images/people-typing-codes.png"> -->
    </div>

    <div class="space-x-8 my-10 px-10 flex">
      <div class="w-full">
        <h1 class="text-5xl text-orange mb-5">Articles</h1>
        <div class="bg-orange rounded-md shadow-xl p-4">
          <div v-if="articles">
            <ArticleCard
              v-for="entry of articles.user.publication.posts"
              :key="entry.slug"
              :cover-image="entry.coverImage"
              :slug="entry.slug"
              :title="entry.title"
              :brief="entry.brief"
              :content-markdown="entry.contentMarkdown"
            />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>
import Vue from 'vue'
import { gql } from 'graphql-tag'
import 'nuxt-graphql-request'

export default Vue.extend({
  name: 'IndexPage',
  layout: 'defaultLayout',
  async asyncData({ $graphql }) {
    const articleCollectionQuery = gql`
      query {
        user(username: "kavinjey") {
          username
          name
          tagline
          coverImage
          _id
          publication {
            _id
            domain
            posts {
              title
              coverImage
              brief
              contentMarkdown
            }
          }
        }
      }
    `
    const articles = await $graphql.hashnode.request(articleCollectionQuery)
    return {
      articles,
    }
  },
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

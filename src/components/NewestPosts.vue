<template>
  <v-container
    pa-0
    mb-4
  >
    <base-subheading>Newest Blog Posts</base-subheading>
    <v-layout
      v-for="(article, i) in articles.slice(11, 14)"
      :key="i"
      align-center
      mb-4
    >
      <v-img
        :src="require(`@/assets/articles/${article.hero}`)"
        class="mr-3"
        height="36"
        max-width="36"
      />
      <div>
        <div class="subheading">
          Article Title
        </div>
        <div class="caption">
          Date
        </div>
      </div>
    </v-layout>
  </v-container>
</template>

<script>
  // Utilities
  import {
    mapState
  } from 'vuex'

  export default {
    computed: {
      ...mapState(['articles'])
    }
  }
</script>

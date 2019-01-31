<template>
  <v-container py-0>
    <base-subheading>Newest Blog Posts</base-subheading>
    <v-layout
      v-for="(article, i) in articles.slice(0, 3)"
      :key="i"
      align-center
      mb-4
    >
      <base-card
        class="mr-3"
        color="grey lighten-2"
        height="36"
        width="36"
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

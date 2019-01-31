<template>
  <v-container
    pa-0
    pr-3
    grid-list-md
  >
    <base-subheading>On Instagram</base-subheading>
    <v-layout wrap>
      <v-flex
        v-for="(post, i) in posts"
        :key="i"
        xs4
      >
        <base-card
          tag="a"
          :href="post.href"
          height="88"
          color="grey lighten-2"
        >
          <v-img
            v-if="post.src"
            :src="post.src"
          />
        </base-card>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
  export default {
    data: () => ({
      posts: [
        { src: '' },
        { src: '' },
        { src: '' },
        { src: '' },
        { src: '' },
        { src: '' }
      ]
    })
  }
</script>

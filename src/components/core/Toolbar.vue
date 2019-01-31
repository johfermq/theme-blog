<template>
  <v-toolbar
    app
    flat
  >
    <v-btn
      v-for="(link, i) in links"
      :key="i"
      :to="link.to"
      flat
      @click="onClick($event, item)"
    >
      {{ link.text }}
    </v-btn>
    <v-spacer />
    <v-text-field
      append-icon="mdi-magnify"
      flat
      solo-inverted
      style="max-width: 300px;"
    />
  </v-toolbar>
</template>

<script>
  // Utilities
  import {
    mapGetters
  } from 'vuex'

  export default {
    computed: {
      ...mapGetters(['links'])
    },

    methods: {
      onClick (e, item) {
        e.stopPropagation()

        if (item.to || !item.href) return

        this.$vuetify.goTo(item.href)
      }
    }
  }
</script>

<template>
  <v-footer
    height="108"
    dark
  >
    <v-container mx-auto>
      <v-layout>
        <v-btn
          v-for="(item, i) in items"
          :key="i"
          fab
          small
          color="primary"
          class="ml-0 v-btn--social-icon mr-3"
          :href="item.href"
          target="_blank"
        >
          <v-icon v-text="item.icon" />
        </v-btn>
        <v-spacer />
        <v-btn
          fab
          small
          color="primary"
          class="mr-0 v-btn--social-icon"
          title="Go to top"
          @click="$vuetify.goTo(0)"
        >
          <v-icon>mdi-chevron-up</v-icon>
        </v-btn>
      </v-layout>
    </v-container>
  </v-footer>
</template>

<script>
  export default {
    data: () => ({
      items: [
        {
          href: '#!',
          icon: 'mdi-twitter'
        },
        {
          href: '#!',
          icon: 'mdi-instagram'
        },
        {
          href: '#!',
          icon: 'mdi-facebook'
        },
        {
          href: '#!',
          icon: 'mdi-google-plus'
        },
        {
          href: '#!',
          icon: 'mdi-reddit'
        },
        {
          href: '#!',
          icon: 'mdi-discord'
        },
        {
          href: '#!',
          icon: 'mdi-pinterest'
        }
      ]
    })
  }
</script>

<style lang="scss" scoped>
.v-btn--social-icon {
  border-radius: 2px !important;
}
</style>

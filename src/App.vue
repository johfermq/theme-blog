<template>
  <v-app>
    <core-toolbar />

    <core-drawer />

    <core-view />

    <core-footer />

    <core-cta />
  </v-app>
</template>

<script>

  export default {
    name: 'App',
    components: {
      CoreCta: () => import('@/components/core/Cta'),
      CoreDrawer: () => import('@/components/core/Drawer'),
      CoreFooter: () => import('@/components/core/Footer'),
      CoreToolbar: () => import('@/components/core/Toolbar'),
      CoreView: () => import('@/components/core/View')
    },
    data () {
      return {
      //
      }
    }
  }
</script>

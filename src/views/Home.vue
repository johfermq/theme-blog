<template>
  <div id="home">
    <feed />

    <about />

    <social />
  </div>
</template>

<script>
  export default {
    name: 'Home',

    components: {
      About: () => import('@/components/home/About'),
      Feed: () => import('@/components/home/Feed'),
      Social: () => import('@/components/home/Social')
    }
  }
</script>

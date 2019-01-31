<template>
  <v-flex
    xs12
    :class="classes"
  >
    <base-card
      height="350"
      color="grey lighten-1"
    >
      <!--  -->
    </base-card>
  </v-flex>
</template>

<script>
  export default {
    props: {
      size: {
        type: Number,
        required: true
      }
    },

    computed: {
      classes () {
        return {
          'md6': this.size === 2,
          'md4': this.size === 3
        }
      }
    }
  }
</script>

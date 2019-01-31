<template>
  <h2
    class="subheading text-uppercase font-weight-medium"
    v-bind="$attrs"
    v-on="$listeners"
  >
    <slot />
  </h2>
</template>

<script>
  export default {
    name: 'BaseSubheading',

    inheritAttrs: false
  }
</script>

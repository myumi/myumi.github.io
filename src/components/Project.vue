<template>
  
</template>

<script>
export default {
  name: 'Project',
  props: {
    name: {
      type: String,
      required: true
    },
    subheader: {
      type: String,
      required: true,
    },
    description: {
      type: String,
      required: true,
    },
    image: {
      type: Object,
      default: undefined
    }
  }
}
</script>

<style lang="scss">

</style>
<template>
  <div class="cms-element-image">
    <img :src="data.media.url">
  </div>
</template>

<script>
export default {
  props: {
    config: {
      type: Object,
      default: () => {}
    },

    data: {
      type: Object,
      default: () => {}
    }
  }
}
</script>

<style scoped>
.cms-element-image {
  /* border: solid 1px #666; */
  width: 100%;
}

.cms-element-image > img {
    max-width: 100%;
}
</style>

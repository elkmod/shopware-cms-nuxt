<template>
  <div class="cms-element-text" v-html="data.content">
    <p>{{ data.content }}</p>
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
.cms-element-text {
  /* border: solid 1px #666; */
  width: 100%;
}
</style>

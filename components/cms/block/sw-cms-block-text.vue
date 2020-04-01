<template>
  <div class="cms-block-text" v-html="slots[0].translated.config.content.value">
    {{ slots[0].translated.config.content.value }}
  </div>
</template>

<script>
export default {
  props: {
    slots: {
      type: Array,
      default: () => []
    }
  }
}
</script>

<style scoped>
.cms-block-text {
  /* border: solid 1px #666; */
  margin: 20px;
}
</style>

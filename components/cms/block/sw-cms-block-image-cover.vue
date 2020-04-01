<template>
  <div class="cms-block-image-cover">
    <SwCmsElementImage :config="resolveSlot('image').config" :data="resolveSlot('image').data" />
  </div>
</template>

<script>
import Elements from '~/components/cms/element'

export default {
  components: Elements,

  props: {
    slots: {
      type: Array,
      default: () => []
    }
  },

  data () {
    return {
      config: {
        image: {}
      }
    }
  },

  methods: {
    resolveSlot (slotName) {
      return this.slots[this.slots.findIndex(e => e.slot === slotName)]
    }
  }
}
</script>

<style scoped>
.cms-block-image-cover {
  /* border: solid 1px #666; */
  margin: 20px;
}
</style>

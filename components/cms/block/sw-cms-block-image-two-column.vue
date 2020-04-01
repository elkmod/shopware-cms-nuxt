<template>
  <div class="cms-block-image-two-column">
    <div class="left">
      <SwCmsElementImage :config="resolveSlot('left').config" :data="resolveSlot('left').data" />
    </div>

    <div class="right">
      <SwCmsElementImage :config="resolveSlot('right').config" :data="resolveSlot('right').data" />
    </div>
  </div>
</template>

<script>
import SwCmsElementImage from '~/components/cms/element/sw-cms-element-image'

export default {
  components: {
    SwCmsElementImage
  },

  props: {
    slots: {
      type: Array,
      default: () => []
    }
  },

  data: () => {
    return {
      config: {
        left: {},
        right: {}
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
.cms-block-image-two-column {
  /* border: solid 1px #666; */
  display: flex;
  align-items: center;
  margin: 0px;
}

.cms-block-image-two-column > div {
  margin: 20px;
  flex-grow: 1;
  width: 50%;
  text-align: center;
}
</style>

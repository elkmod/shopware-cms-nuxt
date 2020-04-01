<template>
  <div class="cms-block-image-text">
    <div class="left">
      <component :is="getComponentByType(resolveSlot('left').type)" :data="resolveSlot('left').data" :config="resolveSlot('left').config" />
    </div>

    <div class="right">
      <component :is="getComponentByType(resolveSlot('right').type)" :data="resolveSlot('right').data" :config="resolveSlot('right').config" />
    </div>
  </div>
</template>

<script>
import Elements from '~/components/cms/element'

const elementMap = {
  text: 'SwCmsElementText',
  image: 'SwCmsElementImage'
}

export default {
  components: Elements,

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
    },

    getComponentByType: type => elementMap[type]
  }
}
</script>

<style scoped>
.cms-block-image-text {
  /* border: solid 1px #666; */
  display: flex;
  align-items: center;
  margin: 0px;
}

.cms-block-image-text > div {
  margin: 20px;
  flex-grow: 1;
  width: 50%;
  text-align: center;
}
</style>

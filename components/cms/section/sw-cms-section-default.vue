<template>
  <div class="cms-section-default">
    <component :is="getComponentByType(block.type)" v-for="block in blocks" :key="block.id" :slots="block.slots" />
  </div>
</template>

<script>
import Blocks from '~/components/cms/block'

const blockMap = {
  text: 'SwCmsBlockText',
  'image-two-column': 'SwCmsBlockImageTwoColumn',
  'image-cover': 'SwCmsBlockImageCover',
  'image-text': 'SwCmsBlockImageText'
}

export default {
  components: Blocks,

  props: {
    blocks: {
      type: Array,
      default: () => []
    }
  },

  methods: {
    getComponentByType: type => blockMap[type]
  }
}
</script>

<style>
.cms-section-default {
  /* border: solid 1px #666; */
}
</style>

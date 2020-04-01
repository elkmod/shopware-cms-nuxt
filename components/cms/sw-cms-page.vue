<template>
  <div class="cms-page">
    <!-- This part will need to include other types of sections depending on section.type -->
    <SwCmsSectionDefault v-for="section in sections" :key="section.id" :blocks="section.blocks" />
  </div>
</template>

<script>

import Sections from '~/components/cms/section'

export default {
  components: Sections,

  props: {
    sections: {
      type: Array,
      default: () => []
    }
  }
}
</script>

<style>
.cms-page {
  /* border: solid 1px #666; */
}
</style>

<template>
  <div>
    <SwCmsPage :sections="cmsPage.sections" />
  </div>
</template>

<script>
import SwCmsPage from '~/components/cms/sw-cms-page'

export default {
  components: {
    SwCmsPage
  },

  async asyncData ({ $axios }) {
    $axios.setHeader('sw-access-key', 'SWSCMUDKAKHSRXPJEHNOSNHYAG')
    const data = (await $axios.post('https://shopware-2.vuestorefront.io/store-api/v1/pwa/page', {
      path: 'Sports/'
    })).data

    return { cmsPage: data.cmsPage }
  },

  data () {
    return {
      cmsPage: {
      }
    }
  }
}
</script>

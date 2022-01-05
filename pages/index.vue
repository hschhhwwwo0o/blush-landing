<template>
  <the-layout>
    <main>
      <the-title />
      <the-download />
      <the-preview />
      <the-information />
      <the-footer />
    </main>
  </the-layout>
</template>

<script>
import TheLayout from '@/components/TheLayout.vue'
import TheTitle from '@/components/TheTitle.vue'
import TheDownload from '@/components/TheDownload.vue'
import ThePreview from '@/components/ThePreview.vue'
import TheInformation from '@/components/TheInformation.vue'
import TheFooter from '@/components/TheFooter.vue'

export default {
  name: 'IndexPage',
  components: {
    TheLayout,
    TheTitle,
    TheDownload,
    ThePreview,
    TheInformation,
    TheFooter,
  },
}
</script>

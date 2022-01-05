<template>
  <the-layout>
    <main>
      <the-title />
      <the-download />
      <the-preview />
    </main>
  </the-layout>
</template>

<script>
import TheLayout from '@/components/TheLayout.vue'
import TheTitle from '@/components/TheTitle.vue'
import TheDownload from '@/components/TheDownload.vue'
import ThePreview from '@/components/ThePreview.vue'

export default {
  name: 'IndexPage',
  components: {
    TheLayout,
    TheTitle,
    TheDownload,
    ThePreview,
  },
}
</script>

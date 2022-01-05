<template>
  <the-layout>
    <main>
      <the-title />
      <the-download />
    </main>
  </the-layout>
</template>

<script>
import TheLayout from '@/components/TheLayout.vue'
import TheTitle from '@/components/TheTitle.vue'
import TheDownload from '@/components/TheDownload.vue'

export default {
  name: 'IndexPage',
  components: {
    TheLayout,
    TheTitle,
    TheDownload,
  },
}
</script>

<template>
  <div class="pt-6 lg:pt-12 flex flex-row gap-10">
    <span
      @click="changeLinksDownloadingVisible"
      :class="`underline text-lg cursor-pointer transition-opacity duration-500 ${
        isOpenDownload ? 'opacity-70' : 'opacity-100'
      }`"
      >Download for Linux</span
    >
    <div v-if="isOpenDownload" class="flex flex-row gap-6 text-lg">
      <a download href="/assets/blush_4.2.2_amd64.deb" class="underline">
        .deb (x64)
      </a>
      <a download href="/assets/blush-4.2.2-1.x86_64.rpm" class="underline">
        .rpm (x64)
      </a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TheDownload',
  data() {
    return {
      isOpenDownload: false,
    }
  },
  methods: {
    changeLinksDownloadingVisible() {
      this.isOpenDownload = !this.isOpenDownload
    },
  },
}
</script>

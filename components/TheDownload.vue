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
      <a
        download
        href="https://drive.google.com/file/d/1SKmHN2ybdK2zPhmOD0VwfYmBQgjoe_ER/view?usp=sharing"
        class="underline"
      >
        .deb (x64)
      </a>
      <a
        download
        href="https://drive.google.com/file/d/1PGfE5NUpYaGm4lLX0OB6K0_VZ4cSALM1/view?usp=sharing"
        class="underline"
      >
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

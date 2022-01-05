<template>
  <div class="pt-6 lg:pt-12 flex flex-row gap-10">
    <span
      :class="`underline text-lg cursor-pointer transition-opacity duration-500 ${
        isOpenDownload ? 'opacity-70' : 'opacity-100'
      }`"
      @click="changeLinksDownloadingVisible"
      >Download for Linux</span
    >
    <div v-if="isOpenDownload" class="flex flex-row gap-6 text-lg">
      <span
        class="underline cursor-pointer"
        @click="
          () =>
            goToDownload(
              'https://drive.google.com/file/d/1SKmHN2ybdK2zPhmOD0VwfYmBQgjoe_ER/view?usp=sharing'
            )
        "
      >
        .deb (x64)
      </span>
      <span
        class="underline cursor-pointer"
        @click="
          () =>
            goToDownload(
              'https://drive.google.com/file/d/1PGfE5NUpYaGm4lLX0OB6K0_VZ4cSALM1/view?usp=sharing'
            )
        "
      >
        .rpm (x64)
      </span>
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
    goToDownload(href) {
      this.$router.push('/thanks-for-downloading')
      setTimeout(() => {
        window.open(String(href))
      }, 1000)
    },
  },
}
</script>

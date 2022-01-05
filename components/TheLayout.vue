<template>
  <div
    class="w-full flex items-center justify-center px-6 sm:px-12 lg:px-32 pt-16 lg:pt-36"
  >
    <div class="w-full max-w-6xl">
      <slot />
    </div>
  </div>
</template>

<script>
export default {
  name: 'TheLayout',
}
</script>

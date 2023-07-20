<template>
  <div class="tw-mb-7">
    <h2 class="tw-text-3xl md:tw-text-4xl tw-font-bold tw-text-neutral-300">
      {{ title }}
    </h2>
    <p v-if="subtitle" class="tw-mt-2 tw-text-base md:tw-text-lg">
      {{ subtitle }}
    </p>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: true,
    },
    subtitle: {
      type: String,
    },
  },
};
</script>

<style scoped>
/* Add your custom styles here */
</style>

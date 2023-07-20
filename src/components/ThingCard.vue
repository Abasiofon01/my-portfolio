<template>
  <a
    :href="href"
    rel="noreferrer"
    target="_blank"
    :class="`tw-p-2 tw-rounded-xl tw-text-neutral-400 tw-bg-neutral-800 hover:tw-bg-${background} hover:tw-shadow-xl tw-transition-all tw-flex tw-items-center`"
  >
    <span
      class="tw-inline-flex tw-items-center tw-justify-center tw-w-8 tw-h-8 md:tw-w-11 md:tw-h-11 tw-bg-neutral-800 tw-rounded-lg tw-mr-3 tw-shrink-0"
      :style="{ backgroundColor: background }"
    >
      <span class="tw-relative tw-w-4 tw-h-4 md:tw-w-6 md:tw-h-6">
        <img :src="icon" alt="icon" />
      </span>
    </span>

    <h4
      class="tw-text-sm md:tw-text-base lg:tw-text-lg tw-font-bold tw-text-neutral-200 tw-truncate"
    >
      {{ title }}
    </h4>
  </a>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: true,
    },
    background: {
      type: String,
      default: "#2B5CEA",
    },
    icon: {
      type: String,
      required: true,
    },
    href: {
      type: String,
      required: true,
    },
  },
};
</script>

<style scoped>
/* Add your custom styles here */
</style>

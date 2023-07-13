<template>
  <a
    :href="href"
    rel="noreferrer"
    target="_blank"
    class="tw-p-5 md:tw-p-8 tw-rounded-2xl tw-bg-gradient-to-tl from-tw-gray-800 to-tw-gray-700 lg:tw-aspect-square tw-text-gray-400 tw-border tw-border-transparent tw-border-opacity-0 hover:tw-border-gray-700 hover:tw-border-opacity-50 hover:tw-shadow-xl hover:tw-from-gray-900 hover:tw-to-gray-800 tw-transition-all"
  >
    <span
      class="tw-inline-flex tw-items-center tw-justify-center tw-w-14 tw-h-14 tw-bg-gray-800 tw-rounded-lg tw-mb-5"
      :style="{ backgroundColor: background }"
    >
      <q-img :src="icon" class="tw-h-6 tw-w-6" :alt="title" />
    </span>

    <h3
      class="tw-text-xl md:tw-text-2xl tw-font-bold tw-text-gray-200 tw-mb-2 md:tw-mb-3"
    >
      {{ title }}
    </h3>
    <p class="tw-text-sm md:tw-text-base">{{ description }}</p>
  </a>

  <div
    class="tw-max-w-sm tw-bg-white tw-border tw-border-gray-200 tw-rounded-lg tw-shadow dark:tw-bg-gray-800 dark:tw-border-gray-700"
  >
    <a href="#">
      <img
        class="tw-rounded-t-lg"
        src="https://cdn.quasar.dev/img/parallax2.jpg"
        alt=""
      />
    </a>
    <div class="tw-p-5">
      <a href="#">
        <h5
          class="tw-mb-2 tw-text-2xl tw-font-bold tw-tracking-tight tw-text-gray-900 dark:tw-text-white"
        >
          Noteworthy technology acquisitions 2021
        </h5>
      </a>
      <p class="tw-mb-3 tw-font-normal tw-text-gray-700 dark:tw-text-gray-400">
        Here are the biggest enterprise technology acquisitions of 2021 so far,
        in reverse chronological order.
      </p>
      <a
        href="#"
        class="tw-inline-flex tw-items-center tw-px-3 tw-py-2 tw-text-sm tw-font-medium tw-text-center tw-text-white tw-bg-blue-700 tw-rounded-lg hover:tw-bg-blue-800 focus:tw-ring-4 focus:tw-outline-none focus:tw-ring-blue-300 dark:tw-bg-blue-600 dark:hover:tw-bg-blue-700 dark:focus:tw-ring-blue-800"
      >
        Read more
        <svg
          class="tw-w-3.5 tw-h-3.5 tw-ml-2"
          aria-hidden="true"
          xmlns="http://www.w3.org/2000/svg"
          fill="none"
          viewBox="0 0 14 10"
        >
          <path
            stroke="currentColor"
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M1 5h12m0 0L9 1m4 4L9 9"
          />
        </svg>
      </a>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: {
      type: String,
      required: true,
    },
    description: {
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

<template>
  <footer class="tw-mt-28">
    <div class="tw-flex tw-items-center tw-justify-between tw-mb-3">
      <div class="tw-mt-0 tw-order-1">
        <div
          class="tw-text-left tw-text-xs tw-text-gray-400 tw-flex tw-items-center"
        >
          <router-link to="/">
            <a
              aria-label="Abasiofon Udonkang"
              class="text-white opacity-30 hover:opacity-100"
            >
              <!-- <Logo class="h-9 w-auto" /> -->
              Abasiofon
            </a>
          </router-link>
        </div>
      </div>
    </div>
    <div>
      <div
        class="tw-py-3 tw-border-t tw-border-gray-800 tw-flex tw-justify-between sm:tw-items-center"
      >
        <div
          class="tw-flex tw-justify-center tw-space-x-6 sm:tw-order-2 tw-text-sm"
        >
          <span>{{ currentYear }}</span>
          <span>Abasiofon Udonkang</span>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
// import Logo from "@/components/Logo.vue"; // Replace with the path to your Logo component

export default {
  components: {
    // Logo,
  },
  data() {
    return {
      currentYear: new Date().getFullYear(),
    };
  },
};
</script>

<style scoped>
/* Add your custom styles here */
</style>

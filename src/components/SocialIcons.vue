<template>
  <div
    class="tw-flex tw-flex-wrap tw-justify-between sm:tw-justify-start tw-space-x-0 sm:tw-space-x-7"
  >
    <SocialLink href="https://twitter.com/_abasiofon" />
    <SocialLink href="https://github.com/abasiofon01" />
    <SocialLink href="mailto:abasiofonudonkang@gmail.com" />
    <SocialLink href="https://linkedin.com/in/abasiofon-udonkang" />
  </div>
</template>
<script>
import SocialLink from "./SocialLink.vue";

export default {
  name: "SocialIcons",
  components: { SocialLink },
};
</script>
<style lang=""></style>

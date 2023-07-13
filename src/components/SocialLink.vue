<template>
  <a
    :href="href"
    rel="noreferrer"
    target="_blank"
    :class="getLinkClasses"
    :aria-label="href"
  >
    <template v-if="href.includes('twitter')">
      <TwitterIcon class="tw-w-8 tw-h-8" />
    </template>

    <template v-else-if="href.includes('mailto')">
      <EmailIcon class="tw-w-8 tw-h-8" />
    </template>
    <template v-else-if="href.includes('github')">
      <GithubIcon class="tw-w-8 tw-h-8" />
    </template>
    <template v-else-if="href.includes('linkedin')">
      <LinkedInIcon class="tw-w-8 tw-h-8" />
    </template>
  </a>
</template>

<script>
import TwitterIcon from "../components/TwitterIcon.vue";
import EmailIcon from "../components/EmailIcon.vue";
import GithubIcon from "../components/GitHubIcon.vue";
import LinkedInIcon from "./LinkedInIcon.vue";

export default {
  name: "SocialLink",
  props: {
    href: {
      type: String,
      required: true,
    },
  },
  computed: {
    getLinkClasses() {
      return [
        "tw-text-gray-600",
        "hover:tw-bg-gray-700",
        "hover:tw-text-white",
        "tw-p-3",
        "tw-rounded-full",
        "tw-transition-colors",
        "tw-group",
      ];
    },
  },
  components: {
    TwitterIcon,
    EmailIcon,
    GithubIcon,
    LinkedInIcon,
    LinkedInIcon,
  },
};
</script>

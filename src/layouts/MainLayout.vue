<template>
  <q-layout view="lHh Lpr lFf">
    <header>
      <div
        className=" tw-animate-pulse tw-w-full tw-flex tw-justify-center tw-my-6"
      >
        <router-link
          class="tw-text-gray-600 hover:tw-text-white tw-transition-colors"
          to="/"
          aria-label="Abasiofon Udonkang"
        >
          <Logo />
        </router-link>
      </div>
    </header>

    <FooterSection />

    <q-page-container>
      <q-page-scroller
        position="bottom-right"
        :scroll-offset="150"
        :offset="[18, 18]"
      >
        <q-btn
          fab
          icon="keyboard_arrow_up"
          style="background-color: #5a649c; color: white"
        />
      </q-page-scroller>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import IndexPage from "src/pages/IndexPage.vue";
import { defineComponent } from "vue";
import FooterSection from "src/components/FooterSection.vue";
import Logo from "src/components/PageLogo.vue";

export default defineComponent({
  name: "MainLayout",

  components: {
    // FooterSection,
    Logo,
  },
});
</script>

<style lang="scss"></style>

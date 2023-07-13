<template>
  <q-page
    class="tw-max-w-5xl tw-mx-auto tw-px-4 sm:tw-px-6 lg:tw-px-8 tw-mb-10"
  >
    <div
      class="mt-28 tw-animate-fade-up tw-animate-duration-1000 tw-animate-delay-300"
    >
      <div>
        <TagLine />
        <h1
          class="tw-text-6xl md:tw-text-8xl tw-font-extrabold tw-text-white tw-mb-16 tw-leading-tight tw-cursor-default"
        >
          Abasiofon Udonkang
        </h1>
      </div>
      <div class="tw-flex tw-items-center tw-gap-4">
        <h2
          class="tw-text-2xl md:tw-text-3xl tw-font-bold tw-text-gray-500 tw-my-6 tw-inline-flex tw-items-center tw-group tw-cursor-default"
        >
          Don't be a stranger
        </h2>

        <SocialIcons />
      </div>
    </div>
    <!-- <div class="tw-mt-36">
      <SectionTitle title="Projects" />
      <div
        class="tw-grid tw-grid-cols-2 md:tw-grid-cols-3 tw-gap-3 md:tw-gap-7 lg:tw-gap-9"
      >
        <ProjectCard
          title="tipybit"
          description="Receive donations and sell products in Bitcoins."
          background="#2B5CEA"
          icon="../assets/projects/tipybit.svg"
          href="https://tipybit.com"
        />
        <ProjectCard
          title="Sedelab"
          description="Platform to pay for tickets and subscriptions to soccer teams."
          background="#4A90E2"
          icon="../assets/projects/sedelab.svg"
          href="https://sedelab.com"
        />
        <ProjectCard
          title="qpasó"
          description="All the news and information from Argentina in a single page."
          background="#F8532D"
          icon="../assets/projects/qpaso.svg"
          href="https://qpaso.ar"
        />
        <ProjectCard
          title="WarWordly"
          description="1v1 multiplayer word guessing game."
          background="#4E60D5"
          icon="../assets/projects/warwordly.svg"
          href="https://warwordly.com"
        />
        <ProjectCard
          title="Quema Labs"
          description="WordPress shop for premium and free themes."
          background="#000000"
          icon="../assets/projects/quemalabs.svg"
          href="https://quemalabs.com"
        />
        <ProjectCard
          title="Pickerist"
          description="Instagram giveaways by selecting a random comment."
          background="#5A649C"
          icon="../assets/projects/pickerist.svg"
          href="https://pickerist.com"
        />
        <ProjectCard
          title="Dolawz"
          description="Streetwear clothing brand."
          background="#000000"
          icon="../assets/projects/dolawz.svg"
          href="https://dolawz.com"
        />
        <ProjectCard
          title="Resim"
          description="Mac App for resizing image with just drag & drop."
          background="#138DD6"
          icon="../assets/projects/resim.svg"
          href="https://nicoandrade.github.io/resim/"
        />
        <ProjectCard
          title="Birlab"
          description="SaaS solution for micro craft beer producers."
          background="#3193FE"
          icon="/public/images/projects/birlab.svg"
          href="https://birlab.com"
        />
        <ProjectCard
          title="Birtap"
          description="An app to help user choose the right beer from a bar."
          background="#EF7623"
          icon="/public/images/projects/birtap.svg"
          href="https://birtap.com"
        />
        <ProjectCard
          title="Dolapp"
          description="Mac App that shows the price between USD/ARS."
          background="#20B490"
          icon="/public/images/projects/dolapp.svg"
          href="https://nicoandrade.github.io/dolapp/"
        />
      </div>
    </div>
    <ProjectCarousel /> -->

    <div class="tw-mt-36">
      <SectionTitle title="Development" subtitle="Tools I work with" />

      <h3
        class="tw-border-b tw-border-gray-800 tw-text-lg tw-font-bold tw-text-gray-400 tw-pb-3 tw-mb-4"
      >
        Tools
      </h3>
      <div
        class="tw-grid tw-grid-cols-2 md:tw-grid-cols-4 tw-gap-2 lg:tw-gap-4 tw-mb-10"
      >
        <ThingCard
          v-for="(tool, index) in tools"
          :key="tool.id"
          :class="[
            tool.class,
            `tw-animate-fade-right tw-animate-duration-${
              100 + index * 1000
            } tw-animate-delay-${100 + index * 4000}ms`,
          ]"
          :title="tool.title"
          :background="tool.background"
          :icon="tool.icon"
          :href="tool.href"
        />
      </div>

      <h3
        class="tw-border-b tw-border-gray-800 tw-text-lg tw-font-bold tw-text-gray-400 tw-pb-3 tw-mb-4"
      >
        Services
      </h3>
      <div
        class="tw-grid tw-grid-cols-2 md:tw-grid-cols-4 tw-gap-2 lg:tw-gap-4 tw-mb-10"
      >
        <ThingCard
          v-for="service in services"
          :key="service.id"
          :title="service.title"
          :background="service.background"
          :class="[service.class]"
          :icon="service.icon"
          :href="service.href"
        />
      </div>
    </div>
  </q-page>
</template>

<script>
import { defineComponent } from "vue";
import TagLine from "src/components/TagLine.vue";
import SocialIcons from "src/components/SocialIcons.vue";
import SectionTitle from "src/components/SectionTitle.vue";
import { tools, services } from "../data/data";
import ProjectCard from "src/components/ProjectCard.vue";
import ThingCard from "src/components/ThingCard.vue";
import ProjectCarousel from "src/components/ProjectCarousel.vue";

export default defineComponent({
  name: "IndexPage",
  components: {
    TagLine,
    SocialIcons,
    SectionTitle,
    // ProjectCard,
    ThingCard,
    // ProjectCarousel,
  },

  data() {
    return {
      tools: tools,
      services: services,
      intersect: false,
    };
  },
});
</script>

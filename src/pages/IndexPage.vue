<template>
  <q-page
    class="tw-max-w-5xl tw-mx-auto tw-px-4 sm:tw-px-6 lg:tw-px-8 tw-mb-10"
  >
    <div
      class="tw-mt-28 tw-animate-fade-up tw-animate-duration-1000 tw-animate-delay-300"
    >
      <div>
        <TagLine />
        <h1
          class="tw-text-6xl md:tw-text-8xl tw-font-extrabold tw-text-neutral-300 tw-mb-16 tw-leading-tight tw-cursor-default"
        >
          Abasiofon Udonkang
        </h1>
      </div>
      <div class="tw-flex tw-items-center tw-gap-4">
        <h2
          class="tw-text-2xl md:tw-text-3xl tw-font-bold tw-text-neutral-500 tw-my-6 tw-inline-flex tw-items-center tw-group tw-cursor-default"
        >
          Don't be a stranger
        </h2>

        <SocialIcons />
      </div>
    </div>

    <div class="tw-mt-36">
      <SectionTitle title="Projects" />
      <div class="projects-wrapper">
        <div
          v-for="project in projects"
          :key="`${project.title}_${project.id}`"
        >
          <!-- <q-intersection
            :root="listEl"
            transition="scale"
            transition-duration="300"
          > -->
          <ProjectCard
            :title="project.title"
            :description="project.description"
            :image="project.image"
            :href="project.href"
            :tools="project.tools"
          />
          <!-- </q-intersection> -->
        </div>
        <!-- <ProjectCard
          title="Analog Clock"
          description="Platform to pay for tickets and subscriptions to soccer teams."
          image="/public/images/projects/analog_clock.png"
          href="https://lovely-analog-clock.netlify.app"
        /> -->
      </div>
    </div>

    <div class="tw-mt-36">
      <SectionTitle title="Development" subtitle="Tools I work with" />

      <h3
        class="tw-border-b tw-border-neutral-800 tw-text-lg tw-font-bold tw-text-neutral-400 tw-pb-3 tw-mb-4"
      >
        Tools
      </h3>
      <q-intersection
        :root="listEl"
        transition-duration="600"
        transition="scale"
      >
        <div
          class="tw-grid tw-grid-cols-2 md:tw-grid-cols-4 tw-gap-2 lg:tw-gap-4 tw-mb-10"
        >
          <ThingCard
            v-for="tool in tools"
            :key="tool.id"
            :class="[tool.class]"
            :title="tool.title"
            :background="tool.background"
            :icon="tool.icon"
            :href="tool.href"
          />
        </div>
      </q-intersection>

      <q-intersection
        :root="listEl"
        transition-duration="700"
        transition="scale"
      >
        <h3
          class="tw-border-b tw-border-neutral-800 tw-text-lg tw-font-bold tw-text-neutral-400 tw-pb-3 tw-mb-4"
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
      </q-intersection>
    </div>
  </q-page>
</template>

<script>
import { defineComponent } from "vue";
import TagLine from "src/components/TagLine.vue";
import SocialIcons from "src/components/SocialIcons.vue";
import SectionTitle from "src/components/SectionTitle.vue";
import { tools, services, projects } from "../data/data";
import ProjectCard from "src/components/ProjectCard.vue";
import ThingCard from "src/components/ThingCard.vue";
import { ref, computed } from "vue";

export default defineComponent({
  name: "IndexPage",
  components: {
    TagLine,
    SocialIcons,
    SectionTitle,
    ProjectCard,
    ThingCard,
  },

  data() {
    return {
      tools: tools,
      services: services,
      projects: projects,
      intersect: false,

      myListRef: null,
    };
  },
  computed: {
    listEl() {
      return this.myListRef ? this.myListRef.$el : null;
    },
  },
});
</script>
<style lang="scss" scoped></style>

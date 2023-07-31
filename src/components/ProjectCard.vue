<template>
  <div class="card-container">
    <div class="card">
      <div class="img-content">
        <img :src="image" alt="" />
      </div>
      <div class="content">
        <span class="title">{{ title }}</span>
        <span>
          {{ description }}
        </span>
        <q-btn
          :href="href"
          class="tw-self-start tw-bg-neutral-500 tw-text-neutral-200"
          >{{ buttonText }}</q-btn
        >

        <div class="tw-pt-4 tw-pb-2">
          <!-- <span
            class="tw-inline-block tw-bg-neutral-200 tw-rounded-full tw-px-3 tw-py-1 tw-text-sm tw-font-semibold tw-text-neutral-700 tw-mr-2 mb-2"
            >#HTML</span
          > -->
          <div>
            <span
              v-for="tool in tools"
              :key="tool"
              class="tw-inline-block tw-bg-neutral-200 tw-rounded-full tw-px-3 tw-py-1 tw-text-sm tw-font-semibold tw-text-neutral-700 tw-mr-2 mb-2"
              >#{{ tool }}</span
            >
          </div>
        </div>
      </div>
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
    buttonText: {
      type: String,
      default: "View Project",
    },
    image: {
      type: String,
      required: true,
    },
    icon: {
      type: String,
    },
    href: {
      type: String,
      required: true,
    },
    tools: {
      type: Array,
      required: true,
    },
  },
};
</script>

<style lang="scss" scoped>
.card-container {
  // width: 300px;
  // height: 300px;
  position: relative;
  border-radius: 10px;
}

.card-container::before {
  content: "";
  z-index: -1;
  position: absolute;
  inset: 0;
  // background: linear-gradient(-45deg, #f89b29 0%, #ff0f7b 100%);
  // transform: translate3d(0, 0, 0) scale(0.95);
  filter: blur(20px);
}

.card {
  width: 100%;
  height: 100%;
  border-radius: inherit;
  overflow: hidden;
}

.card .img-content {
  width: 100%;
  height: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  // background: linear-gradient(-45deg, #f89b29 0%, #ff0f7b 100%);
  // transition: scale 0.6s, rotate 0.6s, filter 1s;
}

.card .img-content img {
  width: 100%;
  height: 100%;
  // fill: #e8e8e8;
  filter: brightness(55%);
  object-fit: cover;
  transition: all 0.6s cubic-bezier(0.23, 1, 0.32, 1);
}

.card .content {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  // align-items: center;
  justify-content: flex-end;
  // text-align: center;
  gap: 10px;
  color: #e8e8e8;
  padding: 20px;
  line-height: 1.5;
  border-radius: 5px;
  opacity: 0;
  // pointer-events: none;
  transform: translateY(50px);
  transition: all 0.6s cubic-bezier(0.23, 1, 0.32, 1);

  @apply hover:tw-animate-fade-up;
}

.card:hover .content {
  opacity: 1;
  // transform: translateY(0);
}

.card:hover .img-content {
  // scale: 1.2;
  filter: blur(1px);
}

.title {
  @apply tw-text-xl md:tw-text-2xl tw-font-bold tw-text-neutral-300 tw-mb-2 md:tw-mb-3;
  // position: absolute;
  // inset: auto auto 30px 30px;
  text-transform: uppercase;
}

.description {
  @apply tw-text-sm md:tw-text-base tw-text-neutral-300;
}
</style>

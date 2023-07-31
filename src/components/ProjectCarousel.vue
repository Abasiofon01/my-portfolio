<template lang="">
  <q-carousel thumbnails animated v-model="slide" height="400px">
    <q-carousel-slide
      :name="1"
      img-src="https://cdn.quasar.dev/img/mountains.jpg"
    >
    </q-carousel-slide>
    <q-carousel-slide
      :name="2"
      img-src="https://cdn.quasar.dev/img/parallax1.jpg"
    >
    </q-carousel-slide>
    <q-carousel-slide
      :name="3"
      img-src="https://cdn.quasar.dev/img/parallax2.jpg"
    >
    </q-carousel-slide>
  </q-carousel>
</template>
<script>
import { ref } from "vue";

export default {
  setup() {
    return {
      slide: ref(1),
    };
  },
};
</script>
<style lang="scss" scoped>
.custom-caption {
  text-align: center;
  padding: 12px;
  color: white;
  background-color: rgba(0, 0, 0, 0.3);
}

.q-carousel__navigation {
  top: 0px !important;
  bottom: 100px !important;
}
</style>

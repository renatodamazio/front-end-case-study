<template>
  <carousel
    v-if="users.length !== 0"
    :settings="settings"
    :breakpoints="breakpoints"
  >
    <slide v-for="user in users" :key="user.id">
      <Card :props="user" />
    </slide>

    <template #addons>
      <navigation />
    </template>
  </carousel>
</template>

<style lang="scss">
.carousel {
  &__slide {
    align-items: flex-start;
  }

  &__next,
  &__prev {
    background-color: var(--ui-card-button-color);
    box-shadow: 0px 4px 8px var(--ui-card-button-shadow);
    background-image: url("@/assets/images/carousel-arrow-navigation.svg");
    background-position: center center;
    background-repeat: no-repeat;
    width: 40px;
    height: 40px;
    top: 100px;
    transform: none;
    transition: 0.5s ease-in-out;
    overflow: hidden;

    @media screen and (max-width: 700px) {
      display: none !important;
    }

    &:hover {
      background-color: var(--ui-card-button-hover);
    }

    &:active {
      background-color: var(--ui-card-button-active);
    }

    svg {
      display: none;
    }

    &--in-active {
      background-color: var(--ui-card-button-inactive) !important;

      &::before {
        content: "";
        width: 100%;
        height: 100%;
        position: absolute;
        top: 0;
        background-color: var(--ui-card-button-disable);
        opacity: 0.8;
      }
    }
  }

  &__prev {
    left: 2px;
    transform: rotate(180deg);
  }

  &__next {
    right: 2px;
  }
}
</style>

<script lang="ts">
import Card from "./Card.vue";
import { ref } from "vue";
import "vue3-carousel/dist/carousel.css";
import { Carousel, Slide, Navigation } from "vue3-carousel";

export default {
  name: "TheUserCarousel",
  props: ["users"],
  components: {
    Carousel,
    Slide,
    Navigation,
    Card,
  },

  setup() {
    const items = ref([]);
    const settings = ref({
      itemsToShow: 1,
      snapAlign: "center",
    });
    const breakpoints = ref({
      //300px and up
      300: {
        itemsToShow: 1,
        snapAlign: "left",
        wrapAround: true,
      },
      //600px and up
      600: {
        itemsToShow: 1.8,
        snapAlign: "left",
        wrapAround: true,
      },
      // 700px and up
      700: {
        itemsToShow: 1.5,
        snapAlign: "left",
        loop: false,
        wrapAround: true,
      },

      1220: {
        itemsToShow: 2,
        snapAlign: "center",
      },
      // 1024 and up
      1024: {
        itemsToShow: 3,
        snapAlign: "start",
      },

      1600: {
        itemsToShow: 4,
        snapAlign: "start",
      },
    });

    return {
      settings,
      breakpoints,
      items,
    };
  },
};
</script>

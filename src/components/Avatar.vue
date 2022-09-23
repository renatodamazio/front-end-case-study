<template>
  <div class="ui-avatar">
    <img :src="img" :alt="title" @error="setAltImg" />
  </div>
</template>
<style scoped lang="scss">
.ui-avatar {
  width: var(--ui-avatar-size);
  height: var(--ui-avatar-size);
  display: inline-block;
  background-color: var(--ui-color-light-gray);
  border-radius: 100%;
  overflow: hidden;

  img {
    width: 100%;
    height: 100%;
  }
}
</style>
<script lang="ts">
import logo from "@/assets/images/flag.svg";
import { defineComponent } from "vue";

export default defineComponent({
  name: "Avatar",
  props: ["img", "title"],
  setup() {
    const setAltImg = (event: any) => {
      event.target.src = logo;
    };

    return {
      setAltImg,
    };
  },
});
</script>

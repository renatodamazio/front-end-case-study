<template>
   <div v-for="tag, index in _tags">
        <Chips :key="index">{{tag}}</Chips>
    </div>
</template>
<script lang="ts">
import Chips from "./Chips.vue";

export default {
  name: "TheTags",
  props: ["tags"],
  components: {
    Chips,
  },

  data() {
    return {
        _tags: []
    }
  },

  mounted() {
    this._tags =  this.tags ? this.tags.split(",") : [];
  }
};
</script>

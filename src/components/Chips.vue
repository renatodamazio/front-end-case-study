<template>
  <div class="ui-chips">
    <slot></slot>
  </div>
</template>
<style lang="scss">
.ui-chips {
  display: flex;
  height: var(--ui-chips-height);
  align-items: center;
  justify-content: center;
  font-size: var(--ui-chips-fs);
  line-height: var(--ui-chips-line-height);
  font-weight: var(--ui-chips-fw);
  background-color: var(--ui-chips-bg);
  border-radius: var(--ui-chips-border-radius);
  width: fit-content;
  padding: 0 var(--ui-chips-padding);
  white-space: nowrap;
}
</style>
<script lang="ts">
export default {
  name: "chips",
};
</script>

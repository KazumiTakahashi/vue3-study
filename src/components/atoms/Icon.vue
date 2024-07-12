<template>
  <span :class="['icon', `icon-${name}`]"></span>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "Icon",
  props: {
    name: {
      type: String,
      required: true,
    },
  },
});
</script>

<style scoped>
.icon {
  /* Icon styles */
}
</style>

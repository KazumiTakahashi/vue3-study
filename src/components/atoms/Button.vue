<template>
  <button @click="onClick" class="button">{{ label }}</button>
</template>

<script lang="ts">
import "crypto";
import { defineComponent } from "vue";

export default defineComponent({
  name: "Button",
  props: {
    label: {
      type: String,
      required: true,
    },
    onClick: {
      type: Function,
      required: true,
    },
  },
});
</script>

<style scoped>
.button {
  /* Button styles */
}
</style>

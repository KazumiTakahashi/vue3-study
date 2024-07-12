<template>
  <a :href="href" class="link">{{ label }}</a>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "Link",
  props: {
    href: {
      type: String,
      required: true,
    },
    label: {
      type: String,
      required: true,
    },
  },
});
</script>

<style scoped>
.link {
  /* Link styles */
}
</style>

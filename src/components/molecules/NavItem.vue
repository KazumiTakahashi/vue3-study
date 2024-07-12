<template>
  <div class="nav-item">
    <Icon :name="icon" />
    <Link :href="href" :label="label" />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import Icon from "../atoms/Icon.vue";
import Link from "../atoms/Link.vue";

export default defineComponent({
  name: "NavItem",
  components: {
    Icon,
    Link,
  },
  props: {
    icon: {
      type: String,
      required: true,
    },
    label: {
      type: String,
      required: true,
    },
    href: {
      type: String,
      required: true,
    },
  },
});
</script>

<style scoped>
.nav-item {
  display: flex;
  align-items: center;
  padding: 10px 0;
}

.icon {
  margin-right: 10px;
}
</style>

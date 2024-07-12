<template>
  <aside class="sidebar">
    <NavItem icon="home" label="Home" href="/" />
    <NavItem icon="documents" label="Documents" href="/documents" />
    <NavItem icon="contact" label="Contact" href="/contact" />
  </aside>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import NavItem from "../molecules/NavItem.vue";

export default defineComponent({
  name: "Sidebar",
  components: {
    NavItem,
  },
});
</script>

<style scoped>
.sidebar {
  width: 250px;
  background-color: #f4f4f4;
  padding: 15px;
  display: flex;
  flex-direction: column;
}
</style>

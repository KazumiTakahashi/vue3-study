<template>
  <nav class="navbar">
    <NavItem icon="home" label="Home" href="/" />
    <NavItem icon="documents" label="Documents" href="/documents" />
    <NavItem icon="contact" label="Contact" href="/contact" />
  </nav>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import NavItem from "../molecules/NavItem.vue";

export default defineComponent({
  name: "Navbar",
  components: {
    NavItem,
  },
});
</script>

<style scoped>
.navbar {
  background-color: #333;
  padding: 10px;
  display: flex;
}
</style>

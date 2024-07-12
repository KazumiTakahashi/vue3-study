<!-- src/components/templates/MainLayout.vue -->
<template>
  <div class="main-layout">
    <header>
      <Navbar />
    </header>
    <div class="main-content">
      <aside>
        <Sidebar />
      </aside>
      <section>
        <slot></slot>
      </section>
    </div>
    <footer>
      <Footer />
    </footer>
  </div>
</template>

<script lang="ts">
import Footer from "@/components/organisms/Footer.vue";
import Navbar from "@/components/organisms/Navbar.vue";
import Sidebar from "@/components/organisms/Sidebar.vue";
import { defineComponent } from "vue";

export default defineComponent({
  name: "MainLayout",
  components: {
    Navbar,
    Sidebar,
    Footer,
  },
});
</script>

<style scoped>
.main-template {
  display: flex;
}

.main-content {
  flex-grow: 1;
  padding: 20px;
}
</style>

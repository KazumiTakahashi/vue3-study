<template>
  <MainLayout>
    <h1>Memo Home</h1>
    <form @submit.prevent="addMemo">
      <input type="text" v-model="newMemo" placeholder="Enter a memo" />
      <button type="submit">Add Memo</button>
    </form>
    <ul>
      <li v-for="(memo, index) in memos" :key="index">
        {{ memo }}
        <button @click="deleteMemo(index)">Delete</button>
      </li>
    </ul>
  </MainLayout>
</template>

<script lang="ts">
import MainLayout from "@/components/templates/MainLayout.vue";
import { defineComponent } from "vue";

export default defineComponent({
  data() {
    return {
      newMemo: "",
      memos: [] as string[],
    };
  },
  methods: {
    addMemo() {
      if (this.newMemo) {
        this.memos.push(this.newMemo);
        this.newMemo = "";
      }
    },
    deleteMemo(index: number) {
      this.memos.splice(index, 1);
    },
  },
  components: {
    MainLayout,
  },
});
</script>

<style scoped>
h1 {
  color: #333;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  margin-bottom: 10px;
}
button {
  margin-left: 10px;
}
</style>

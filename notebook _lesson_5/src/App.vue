<template>
  <parent-box-cards :card-list="notebooksList" />
</template>

<script>
import ParentBoxCards from "./components/ParentBoxCards.vue";
import { notebooksList } from "./constants/3_data_notebooks";
export default {
  name: "App",
  components: {
    ParentBoxCards,
  },
  data() {
    return {
      notebooksList,
    };
  },
};
</script>

<style></style>

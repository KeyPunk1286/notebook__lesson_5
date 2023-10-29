<template>
  <div class="parent-box">
    <notebook-card
      v-for="card in cardList"
      :key="card.id"
      :cards-content="card"
    />
  </div>
</template>

<script>
import NotebookCard from "./NotebookCard.vue";
export default {
  name: "ParentBoxCards",
  components: {
    NotebookCard,
  },
  props: {
    cardList: {
      type: Array,
      default: () => [],
    },
  },
};
</script>

<style lang="css" scoped></style>

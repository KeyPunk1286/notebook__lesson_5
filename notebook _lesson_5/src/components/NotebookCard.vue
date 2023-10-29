<template>
  <div class="parent-box">
    <img :src="cardsContent.imgSrc" class="parent-box__img" />
    <div class="parent-box__content">
      <a target="_blank" :href="cardsContent.link" class="content__title">{{
        cardsContent.title
      }}</a>
      <div>
        Ваша економія
        <span class="content__discount">{{ cardsContent.discount }}</span>
      </div>
      <div class="content__old-price">{{ cardsContent.oldPrice }}</div>
      <div class="content__prise-by">
        <div class="content__prise">{{ cardsContent.price }}</div>
        <button class="content__by">Купити</button>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "NotebookCard",
  props: {
    cardsContent: {
      type: Object,
      default: () => ({}),
    },
  },
};
</script>

<style lang="css" scoped>
.parent-box {
  max-width: 500px;
  display: flex;
  padding: 10px;
  border-bottom: 1px black solid;
  margin-bottom: 10px;
}
.parent-box__img {
  max-width: 150px;
}
.content__title {
  font-size: 20px;
  color: rgba(50, 50, 190, 0.926);
  transition: color 0.2s;
}
.content__title:hover {
  color: rgba(61, 61, 128, 0.926);
  transition: color 0.2s;
}
.content__discount {
  color: crimson;
}
.content__old-price {
  text-decoration: line-through;
  margin-bottom: 10px;
}
.content__prise-by {
  display: flex;
  justify-content: space-between;
}
.content__prise {
  color: crimson;
  font-size: 20px;
}
.content__by {
  background-color: darkgreen;
  color: aliceblue;
}
</style>

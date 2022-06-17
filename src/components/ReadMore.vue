<template>
  <button>
    <span>Смотреть больше</span>
    <img :src="require('@/assets/icons/arrow-black.svg')" alt="">
  </button>
</template>

<script>
export default {
  name: "ReadMore",
};
</script>

<style lang="scss" scoped>
button {
  display: inline-flex;
  gap: 18px;
  align-items: center;
  border: none;
  background-color: transparent;
  cursor: pointer;

  span {
    font-family: $playfair;
    font-weight: 600;
    font-size: 18px;
    line-height: 55px;
  }
}
</style>

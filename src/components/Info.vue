<template>
  <section>
    <div class="wrap">
      <div v-for="(item, index) in items" :key="index">
        <img :src="require(`@/assets/icons/${item.icon}`)" alt="" />
        <span>{{ item.label }}</span>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Info",
  data() {
    return {
      items: [
        { icon: "correct.svg", label: "Более 30 000 объектов" },
        { icon: "shield.svg", label: "Юридическое сопровождение" },
        { icon: "progress.svg", label: "Динамичное ценообразование" },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
section {
  background: linear-gradient(234.94deg, $dark 8.75%, $black 70.62%);
  color: #fff;
  padding: 24px 0;
  font-size: 1rem;
}

.wrap {
  display: flex;
  justify-content: space-around;
  @include container;

  div {
    display: inherit;
    align-items: center;
    gap: 31.54px;

    span {
      font-family: $firasans;
      line-height: 42px;
      font-weight: 600;
    }
  }
}
</style>

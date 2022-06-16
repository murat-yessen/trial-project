<template>
  <section>
    <div class="wrap">
      <div>
        <img src="./../assets/icons/correct.svg" alt="" />
        <span>Более 30 000 объектов</span>
      </div>
      <div>
        <img src="./../assets/icons/shield.svg" alt="" />
        <span>Юридическое сопровождение</span>
      </div>
      <div>
        <img src="./../assets/icons/progress.svg" alt="" />
        <span>Динамичное ценообразование</span>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Info",
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

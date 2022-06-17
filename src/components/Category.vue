<template>
  <section>
    <div class="wrap">
      <h1>Предложения по категориям</h1>
      <p>
        Безусловно, разбавленное изрядной долей эмпатии, рациональное мышление
        является
      </p>

      <div class="cards">
        <div v-for="(item, index) in items" :key="index" :class="item.class">
          <img :src="require(`@/assets/images/${item.file}`)" alt="" />
          <img
            :src="require('@/assets/images/star.png')"
            v-if="item.star"
            class="star"
            alt=""
          />
          <span>{{ item.label }}</span>
          <img
            :src="require(`@/assets/icons/arrow-black.svg`)"
            class="arrow"
            alt=""
          />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Category",
  data() {
    return {
      items: [
        {
          file: "category_1.png",
          class: "card1",
          label: "Горячие предложения",
          star: true,
        },
        { file: "category_2.png", class: "card2", label: "Апартаменты" },
        {
          file: "category_3.png",
          class: "card3",
          label: "В рассрочку от застройщиков",
        },
        { file: "category_4.png", class: "card4", label: "Наши проекты" },
        {
          file: "category_5.png",
          class: "card5",
          label: "Люкс и преимум уровень",
        },
        { file: "category_6.png", class: "card6", label: "Виллы" },
        { file: "category_7.png", class: "card7", label: "Для инвестиций" },
        {
          file: "category_8.png",
          class: "card8",
          label: "Первая линия от моря",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.wrap {
  @include container;
  padding: 100px 0;

  h1,
  p {
    text-align: center;
  }

  h1 {
    font-family: $playfair;
    font-size: 55px;
    line-height: 55px;
    color: $title-color;
    font-style: normal;
    font-weight: 600;
    margin-bottom: 11px;
  }

  p {
    font-family: $firasans;
    color: $caption-color;
    font-size: 21px;
    font-weight: 400;
    line-height: 40px;
    margin-bottom: 34px;
  }

  .cards {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    grid-template-rows: repeat(3, 1fr);
    grid-column-gap: 30px;
    grid-row-gap: 30px;

    div {
      position: relative;

      span {
        position: absolute;
        left: 0;
        top: 0;
        margin: 30px 20px;
        font-family: $playfair;
        font-style: normal;
        font-weight: 600;
        font-size: 24px;
        line-height: 32px;
      }

      .star {
        position: absolute;
        left: 20px;
        top: 108px;
      }

      .arrow {
        position: absolute;
        left: 20px;
        bottom: 30px;
      }
    }

    img {
      border-radius: 3px;
    }
  }

  .card1 {
    grid-area: 1 / 1 / 3 / 2;
  }
  .card2 {
    grid-area: 3 / 1 / 4 / 2;
  }
  .card3 {
    grid-area: 1 / 2 / 2 / 4;
  }
  .card4 {
    grid-area: 2 / 2 / 3 / 3;
  }
  .card5 {
    grid-area: 2 / 3 / 3 / 4;
  }
  .card6 {
    grid-area: 3 / 2 / 4 / 4;
  }
  .card7 {
    grid-area: 1 / 4 / 2 / 5;
  }
  .card8 {
    grid-area: 2 / 4 / 4 / 5;
  }
}
</style>

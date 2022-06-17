<template>
  <section>
    <div class="wrap">
      <h1>Новые объекты в Турции</h1>
      <p>
        Безусловно, разбавленное изрядной долей эмпатии, рациональное мышление
        является
      </p>

      <div class="cards">
        <div v-for="(item, index) in items" :key="index" class="card">
          <div class="imgs">
            <img
              :src="require(`@/assets/images/${item.file}`)"
              alt=""
              class="bg-image"
            />
            <img
              :src="require('@/assets/images/actions.png')"
              alt=""
              class="actions"
            />
          </div>
          <div class="info">
            <h3>{{ item.title }}</h3>
            <span>ID {{ item.id }}</span>
            <p class="parameters">
              <img :src="require('@/assets/icons/location.svg')" alt="" />
              {{ item.location }}
            </p>
            <p class="parameters">
              <img :src="require('@/assets/icons/area.svg')" alt="" />
              {{ item.area }} м<sup>2</sup>
            </p>
            <p class="parameters">
              <img :src="require('@/assets/icons/door.svg')" alt="" />
              {{ item.door }}
            </p>
            <p class="price">
              {{ formatPrice(item.price.from) }} -
              {{ formatPrice(item.price.to) }} &#8364;
            </p>
          </div>
        </div>
      </div>
      <div class="read-more">
        <ReadMore />
      </div>
    </div>
  </section>
</template>

<script>
import ReadMore from "./ReadMore.vue";

export default {
  name: "NewObjects",
  components: {
    ReadMore,
  },
  data() {
    return {
      items: [
        {
          file: "card1.png",
          title: "Название недвижимости в  две строки",
          id: 23510,
          location: "Алания/Оба",
          area: 132,
          door: "3+1",
          price: {
            from: 902_000,
            to: 1_366_000,
          },
        },
        {
          file: "card2.png",
          title: "Название недвижимости в  две строки",
          id: 23510,
          location: "Алания/Оба",
          area: 132,
          door: "3+1",
          price: {
            from: 902_000,
            to: 1_366_000,
          },
        },
        {
          file: "card3.png",
          title: "Название недвижимости в  две строки",
          id: 23510,
          location: "Алания/Оба",
          area: 132,
          door: "3+1",
          price: {
            from: 902_000,
            to: 1_366_000,
          },
        },
        {
          file: "card4.png",
          title: "Название недвижимости в  две строки",
          id: 23510,
          location: "Алания/Оба",
          area: 132,
          door: "3+1",
          price: {
            from: 902_000,
            to: 1_366_000,
          },
        },
        {
          file: "card5.png",
          title: "Название недвижимости в  две строки",
          id: 23510,
          location: "Алания/Оба",
          area: 132,
          door: "3+1",
          price: {
            from: 902_000,
            to: 1_366_000,
          },
        },
        {
          file: "card6.png",
          title: "Название недвижимости в  две строки",
          id: 23510,
          location: "Алания/Оба",
          area: 132,
          door: "3+1",
          price: {
            from: 902_000,
            to: 1_366_000,
          },
        },
        {
          file: "card7.png",
          title: "Название недвижимости в  две строки",
          id: 23510,
          location: "Алания/Оба",
          area: 132,
          door: "3+1",
          price: {
            from: 902_000,
            to: 1_366_000,
          },
        },
        {
          file: "card8.png",
          title: "Название недвижимости в  две строки",
          id: 23510,
          location: "Алания/Оба",
          area: 132,
          door: "3+1",
          price: {
            from: 902_000,
            to: 1_366_000,
          },
        },
      ],
    };
  },
  methods: {
    formatPrice: function (price) {
      return price.toString().replace(/\B(?=(\d{3})+(?!\d))/g, " ");
    },
  },
};
</script>

<style lang="scss" scoped>
section {
  background-color: $light;

  .wrap {
    @include container;
    padding: 90px 0;

    & > h1,
    & > p {
      text-align: center;
    }

    & > h1 {
      font-family: $playfair;
      font-size: 55px;
      line-height: 55px;
      color: $title-color;
      font-style: normal;
      font-weight: 600;
      margin-bottom: 11px;
    }

    & > p {
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
      grid-template-rows: repeat(2, 1fr);
      grid-column-gap: 30px;
      grid-row-gap: 30px;

      .card {
        box-shadow: 0px 8px 20px rgba(19, 21, 22, 0.1);
        border-radius: 3px;

        .imgs {
          position: relative;

          .bg-image {
            width: 100%;
            border-radius: 3px 3px 0 0;
          }

          .actions {
            position: absolute;
            left: 10px;
            top: 14px;
          }
        }

        .info {
          display: flex;
          flex-direction: column;
          padding: 15px 20px;

          h3,
          .price {
            font-family: $playfair;
            font-style: normal;
            font-weight: 600;
            font-size: 18px;
            line-height: 24px;
          }

          span,
          .parameter {
            font-family: $firasans;
            font-style: normal;
          }

          span {
            margin: 15px 0;
            padding: 6px 12px;
            border-width: 1px;
            border-style: solid;
            border-radius: 3px;
            border-image: linear-gradient(to right, #fcf1b5, #ffbf31) 1;
            width: fit-content;
            font-weight: 600;
          }

          .parameters {
            display: flex;
            align-items: center;
            gap: 10px;
            margin-bottom: 10px;
            font-weight: 400;
            line-height: 19px;
          }

          .price {
            margin-top: 14px;
            font-feature-settings: "pnum" on, "lnum" on;
          }
        }
      }
    }

    .read-more {
        display: flex;
        justify-content: center;
        padding-top: 60px;
    }
  }
}
</style>

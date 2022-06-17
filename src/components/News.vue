<template>
  <section>
    <div class="wrap">
      <h1>Новости и события</h1>
      <p>
        Безусловно, разбавленное изрядной долей эмпатии, рациональное мышление
        является
      </p>

      <div class="cards">
        <div v-for="(item, index) in items" :key="index">
          <div class="imgs">
            <img :src="require(`@/assets/images/${item.img}`)" alt="" />
            <span>{{ item.badge }}</span>
          </div>
          <div class="info">
            <h3>{{ item.label }}</h3>
            <p>{{ item.country }}</p>
            <p>{{ item.description }}</p>
          </div>
        </div>
      </div>

      <button>Смотреть больше</button>
    </div>
  </section>
</template>

<script>
export default {
  name: "News",
  data() {
    return {
      items: [
        {
          img: "news_1.png",
          badge: "Новости",
          label: "Пора золотых цен",
          country: "Анталья",
          description: "Доступная недвижимость в городах Турции с 21 апреля",
        },
        {
          img: "news_2.png",
          badge: "Новости",
          label: "Пора золотых цен",
          country: "Казахстан",
          description: "Доступная недвижимость в городах Турции с 21 апреля",
        },
        {
          img: "news_3.png",
          badge: "События",
          label: "Пора золотых цен",
          country: "Казахстан",
          description: "Доступная недвижимость в городах Турции с 21 апреля",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
section {
  background-color: $light;

  .wrap {
    @include container;
    padding-top: 100px;

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
      grid-template-columns: repeat(3, 1fr);
      grid-template-rows: 1fr;
      grid-column-gap: 30px;

      & > div {
        box-shadow: 0px 8px 20px rgba(19, 21, 22, 0.1);
        border-radius: 3px;
      }

      .imgs {
        position: relative;

        & > img {
          width: 100%;
          border-radius: 3px;
        }

        span {
          position: absolute;
          left: 0;
          top: 10px;
          padding: 11px 30px;
          background-color: $black;
          color: $white;
          font-family: $firasans;
          font-weight: 400;
          font-size: 14px;
          line-height: 16.8px;
          clip-path: polygon(0 0, 100% 0%, calc(100% - 12px) 100%, 0% 100%);
        }
      }

      .info {
        padding: 20px;

        h3,
        p {
          font-family: $firasans;
        }

        p {
          font-weight: 400;
          font-style: normal;
        }

        h3 {
          margin-bottom: 8px;
          font-weight: 600;
          font-size: 18px;
          line-height: 21.6px;

          & + p {
            font-size: 14px;
            line-height: 16.8px;
            color: $news-caption-color;
            margin-bottom: 20px;

            & + p {
              font-size: 16px;
              line-height: 26px;
              color: $title-color;
            }
          }
        }

        & > p {
          text-align: left;
        }
      }
    }
  }
}
</style>

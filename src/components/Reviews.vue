<template>
  <section>
    <div class="wrap">
      <h1>Отзывы</h1>

      <div class="cards">
        <div v-for="(item, index) in items" :key="index" class="card">
          <img
            :src="require(`@/assets/images/${item.file}`)"
            alt=""
            class="bg-image"
          />
          <img
            :src="require('@/assets/images/quote.png')"
            alt=""
            class="quote-img"
          />
          <div class="info">
            <div>
              <h5>{{ item.name }}</h5>
              <span>{{ item.city }}</span>
            </div>
            <p>{{ item.description }}</p>
            <button>Читать далее</button>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Reviews",
  data() {
    return {
      items: [
        {
          file: "review_1.png",
          name: "Иван Орлов",
          city: "Москва",
          description:
            "Идейные соображения высшего порядка, а также реализация намеченных плановых заданий способствует подготовки и реализации соответствующий условий активизации.  Идейные соображения высшего порядка, а также укрепление ",
        },
        {
          file: "review_2.png",
          name: "Иван Орлов",
          city: "Москва",
          description:
            "Идейные соображения высшего порядка, а также реализация намеченных плановых заданий способствует подготовки и реализации соответствующий условий активизации.  Идейные соображения высшего порядка, а также укрепление ",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.wrap {
  @include container;
  padding-bottom: 190px;

  h1 {
    font-family: $playfair;
    font-size: 55px;
    line-height: 55px;
    color: $title-color;
    font-style: normal;
    font-weight: 600;
    margin-bottom: 11px;
    text-align: center;
  }

  .cards {
    display: flex;
    gap: 30px;
    margin-top: 65px;

    & > div {
      position: relative;

      .quote-img {
        position: absolute;
        left: 30px;
        top: -18px;
      }

      .info {
        position: absolute;
        box-shadow: 0px 8px 20px rgba(19, 21, 22, 0.1);
        border-radius: 3px;
        padding: 10px 30px;
        margin-bottom: 190px;
        bottom: -100%;
        width: 80%;
        background-color: $white;
        z-index: 1;

        & > div {
          display: flex;
          justify-content: space-between;

          h5,
          span {
            font-family: $firasans;
            font-style: normal;
            font-size: 16px;
            line-height: 55px;
          }

          h5 {
            font-weight: 600;
          }

          span {
            font-weight: 400;
            color: $info-caption-color;
          }
        }

        p,
        button {
          font-family: $firasans;
          font-style: normal;
        }

        p {
          font-weight: 400;
          font-size: 16px;
          line-height: 26px;
          color: $title-color;
        }

        button {
          margin-top: 20px;
          padding: 15px 42px;
          background-color: transparent;
          border-width: 1px;
          border-style: solid;
          border-image: linear-gradient(to right, #fcf1b5, #ffbf31) 1;
          border-radius: 50%;
          font-weight: 600;
          font-size: 14px;
          line-height: 17px;
          color: $black;
          cursor: pointer;
        }
      }
    }

    img {
      border-radius: 3px;
    }
  }
}
</style>

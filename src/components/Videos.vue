<template>
  <section>
    <div class="wrap">
      <h1>Видео с нашего канала</h1>
      <div class="cards">
        <div v-for="(item, index) in items" :key="index">
          <div class="images">
            <img :src="require(`@/assets/images/${item.img_src}`)" alt="" />
            <img
              :src="require(`@/assets/icons/play.svg`)"
              alt=""
              class="play-btn"
            />
          </div>
          <p>{{ item.label }}</p>
          <div class="stat">
            <img :src="require(`@/assets/icons/eye.svg`)" alt="" />
            <span>{{ item.views }}</span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Videos",
  data() {
    return {
      items: [
        {
          img_src: "video_1.png",
          label:
            "Самая выгодная недвижимость в Стамбуле? Лучшее вложение. Топ-5",
          views: "34 560 просмотров",
        },
        {
          img_src: "video_2.png",
          label:
            "Самая выгодная недвижимость в Стамбуле? Лучшее вложение. Топ-5",
          views: "34 560 просмотров",
        },
        {
          img_src: "video_3.png",
          label:
            "Самая выгодная недвижимость в Стамбуле? Лучшее вложение. Топ-5",
          views: "34 560 просмотров",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
section {
  background-color: $black;
  color: $white;

  .wrap {
    @include container;
    padding: 70px 0 120px 0;

    h1 {
      font-family: $playfair;
      font-size: 55px;
      font-weight: 600;
      line-height: 55px;
      text-align: center;
      margin-bottom: 50px;
    }

    .cards {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      grid-template-rows: 1fr;
      grid-column-gap: 30px;

      img {
        border-radius: 3px;
      }

      .images {
        position: relative;
      }

      .play-btn {
        position: absolute;
        left: 50%;
        top: 50%;
        transform: translate(-50%, -50%);
        cursor: pointer;
      }

      p {
        margin-top: 20px;
        font-family: $firasans;
        font-weight: 600;
        font-size: 18px;
        line-height: 30px;
      }

      .stat {
        display: flex;
        align-items: center;
        gap: 18px;
        margin-top: 20px;

        img {
          margin-top: 0;
        }

        span {
          font-family: $firasans;
          font-weight: 400;
          font-size: 14px;
          line-height: 30px;
          color: $views-color;
        }
      }
    }
  }
}
</style>

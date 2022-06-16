<template>
  <section>
    <div class="wrap">
      <h1>Недвижимость в городах</h1>
      <p>
        Безусловно, разбавленное изрядной долей эмпатии, рациональное мышление
        является
      </p>

      <div class="cards">
        <div class="card1">
          <span class="city-name">Алания</span>
          <span class="price">от 1700 евро</span>
          <img src="./../assets/icons/light-arrow.svg" alt="" />
        </div>
        <div class="card2">
          <span class="city-name">Кипр</span>
          <span class="price">от 1700 евро</span>
          <img src="./../assets/icons/light-arrow.svg" alt="" />
        </div>
        <div class="card3">
          <span class="city-name">Мерсин</span>
          <span class="price">от 1700 евро</span>
          <img src="./../assets/icons/light-arrow.svg" alt="" />
        </div>
        <div class="card4">
          <span class="city-name">Анталия</span>
          <span class="price">от 1700 евро</span>
          <img src="./../assets/icons/light-arrow.svg" alt="" />
        </div>
        <div class="card5">
          <span class="city-name">Стамбул</span>
          <span class="price">от 1700 евро</span>
          <img src="./../assets/icons/light-arrow.svg" alt="" />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "RealEstate",
};
</script>

<style lang="scss" scoped>
section {
  background-color: $white;
}

.wrap {
  @include container;
  padding: 90px 0;

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
}

.cards {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  grid-template-rows: repeat(3, 1fr);
  grid-column-gap: 30px;
  grid-row-gap: 30px;

  div {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    height: 220px;
    border-radius: 3px;
    background-repeat: no-repeat;
    background-size: cover;
    box-shadow: 0 8px 30px rgba(19, 21, 22, 0.1);
    padding: 23px 32px;

    .city-name,
    .price {
      color: $white;
      font-family: $playfair;
    }

    .city-name {
      font-weight: 600;
      font-size: 30px;
      line-height: 26px;
    }

    .price {
      margin-top: 10px;
      font-weight: 400;
      line-height: 21px;
    }

    img {
      height: 26px;
      margin-top: 80px;
    }
  }
}

.card1 {
  grid-area: 1 / 1 / 2 / 2;
  background-image: url("./../assets/images/alanya.png");
}
.card2 {
  grid-area: 1 / 2 / 2 / 3;
  background-image: url("./../assets/images/kipr.png");
}
.card3 {
  grid-area: 2 / 1 / 3 / 2;
  background-image: url("./../assets/images/mersyn.png");
}
.card4 {
  grid-area: 2 / 2 / 3 / 3;
  background-image: url("./../assets/images/antalya.png");
}
.card5 {
  grid-area: 3 / 1 / 4 / 3;
  background-image: url("./../assets/images/stambul.png");
}
</style>

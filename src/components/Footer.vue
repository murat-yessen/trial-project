<template>
  <footer>
    <section class="wrap">
      <h1>Есть вопросы? Пишите нам</h1>
      <form action="#">
        <div class="form-group">
          <label for="name">Ваше имя</label>
          <input type="text" id="name" name="name" placeholder="Введите имя" />
        </div>
        <div class="form-group">
          <label for="telephone">Ваш телефон</label>
          <input
            type="tel"
            id="telephone"
            name="telephone"
            placeholder="+7 ("
          />
        </div>
        <button type="submit">Подобрать жилье</button>
      </form>
      <label for="agree" id="agree-label">
        <input type="checkbox" id="agree" name="agree" />
        <span>Я даю своё согласие на обработку персональных данных</span>
      </label>
    </section>
    <section class="wrap info">
      <div><img src="./../assets/images/logo.png" alt="" /></div>
      <div class="primary">
        <h6>Основной раздел</h6>
        <div>
          <span>Аренда недвижимости</span>
          <span>Продажа недвижимости</span>
          <span>Аренда отелей</span>
          <span>Аренда земли</span>
        </div>
      </div>
      <div class="primary">
        <h6>Дополнительно</h6>
        <div>
          <span>О компании</span>
          <span>Отзывы</span>
          <span>Как мы работаем</span>
          <span>Контакты</span>
        </div>
      </div>
      <div class="address">
        <h5>8 (4872) 704-407</h5>
        <span>Звоните нам</span>
        <button>Обратный звонок</button>

        <h5>Пн-Пт с 9.00 до 18.00</h5>
        <span>График работы</span>

        <h5 class="email">info@mail.ru</h5>
        <span>Для электронных писем</span>
      </div>
    </section>
    <section class="wrap">
      <p class="dimmed-text">2022 (с) Все права защищены</p>
      <div class="developed">
        <p class="dimmed-text">Разработано в</p>
        <img src="./../assets/images/alux.png" alt="" />
      </div>

      <div class="divider"></div>

      <div class="cities">
        <span>Аланя</span>
        <span>Кипр</span>
        <span>Мерсин</span>
        <span>Анталья</span>
        <span>Стамбул</span>
      </div>
    </section>
  </footer>
</template>

<script>
export default {
  name: "Footer",
};
</script>

<style lang="scss" scoped>
footer {
  background-color: $black;
  color: $white;

  .wrap {
    @include container;
    padding-top: 60px;

    & > h1 {
      font-family: $playfair;
      font-size: 55px;
      line-height: 55px;
      color: $white;
      font-style: normal;
      font-weight: 600;
    }

    form {
      margin-top: 50px;
      display: flex;
      gap: 30px;
      align-items: flex-end;

      .form-group {
        display: flex;
        flex-direction: column;

        label,
        input,
        input::placeholder {
          font-family: $firasans;
          font-style: normal;
          font-size: 18px;
          line-height: 22px;
        }

        label {
          font-weight: 600;
          margin-bottom: 5px;
        }

        input {
          width: 410px;
          height: 60px;
          padding: 19px;
          background-color: $white;
          font-size: 18px;
        }

        input,
        input::placeholder {
          font-weight: 400;
        }

        input::placeholder {
          color: #102167;
          opacity: 0.7;
        }
      }

      button {
        background: linear-gradient(
            113.09deg,
            rgba(255, 255, 255, 0.07) -15.73%,
            rgba(192, 101, 0, 0.49) 47.76%,
            rgba(228, 123, 0, 0.21) 95.11%,
            rgba(255, 255, 255, 0) 130.53%
          ),
          linear-gradient(93.98deg, #fcf1b5 -17.56%, #ffbf31 107.31%);
        box-shadow: 0px 10px 30px rgba(245, 177, 51, 0.4);
        border-radius: 3px;
        border: none;
        padding: 21px 40px;
        font-family: $firasans;
        font-style: normal;
        font-weight: 600;
        font-size: 16px;
        line-height: 19px;
        text-align: center;
      }
    }

    #agree-label {
      display: flex;
      align-items: center;
      gap: 12px;
      margin-top: 40px;

      span {
        font-family: $firasans;
        font-style: normal;
        font-weight: 400;
        font-size: 12px;
        line-height: 30px;
      }
    }

    #agree {
      width: 24px;
      height: 24px;
    }

    .dimmed-text {
      text-align: center;
      font-family: $firasans;
      font-style: normal;
      font-weight: 400;
      font-size: 18px;
      line-height: 28px;
      color: #6f7478;
    }

    .developed {
      display: flex;
      justify-content: center;
      align-items: center;
      gap: 10px;
      margin: 60px 0;
    }

    .divider {
      width: 100%;
      height: 2px;
      border-top: 1px solid #282828;
    }

    .cities {
      display: flex;
      justify-content: space-around;
      padding: 40px;

      span {
        font-family: $firasans;
        font-style: normal;
        font-weight: 400;
        font-size: 18px;
        line-height: 22px;
        color: #6f7478;
      }
    }
  }

  .info {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    grid-template-rows: 1fr;
    grid-column-gap: 30px;

    .primary {
      h6 {
        margin-bottom: 25px;
        font-family: $firasans;
        font-style: normal;
        font-weight: 600;
        font-size: 18px;
        line-height: 22px;
        color: #727272;
      }

      div {
        display: flex;
        flex-direction: column;

        span {
          font-family: $firasans;
          font-style: normal;
          font-weight: 400;
          font-size: 18px;
          line-height: 50px;
        }
      }
    }

    .address {
      display: flex;
      flex-direction: column;
      align-items: flex-end;

      h5 {
        font-family: $playfair;
        font-style: normal;
        font-weight: 600;
        font-size: 21px;
        line-height: 30px;
        font-feature-settings: "pnum" on, "lnum" on;
      }

      span {
        margin-bottom: 15px;
        font-family: $firasans;
        font-style: normal;
        font-weight: 400;
        font-size: 16px;
        line-height: 28px;
        color: #6f7478;
      }

      .email {
        color: #7e6745;
      }

      button {
        margin-bottom: 50px;
        padding: 22px 27px;
        background-color: transparent;
        border-width: 1px;
        border-style: solid;
        border-image: linear-gradient(to right, #fcf1b5, #ffbf31) 1;
        border-radius: 50%;
        font-weight: 600;
        font-size: 14px;
        line-height: 17px;
        color: $white;
        cursor: pointer;
      }
    }
  }
}
</style>

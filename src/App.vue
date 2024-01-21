<template>
  <div class="wrapper">
    <header class="header">
      <div class="header__title">
        ARMAGEDDON 2023
      </div>
      <div class="header__text">ООО “Команда им. Б. Уиллиса”.
        Взрываем астероиды с 1998 года.</div>
    </header>
    <main class="main">
      <div class="main__title">Ближайшие подлёты астероидов</div>
      <div class="main__toggle">
        <button>в километрах</button> |
        <button>в лунных орбитах</button>
      </div>
      <div class="main__row">
        <div class="row__items">
          <div class="item">
            <div class="item__title">12 сент 2023</div>
            <div class="item__info"></div>
            <div class="item__button"></div>
          </div>
        </div>
      </div>
      <div class="basket">
        <div class="basket__information">
          <div class="basket__title">Корзина</div>
          2 астероида
        </div>
        <div class="basket__button">
          Отправить
        </div>
      </div>
    </main>
  </div>
</template>

<script>
// import axios from 'axios'
export default {
  mounted () {
    this.test()
  },

  methods: {
    test () {
      // axios.get('https://api.nasa.gov/neo/rest/v1/feed?start_date=2024-01-01&end_date=2024-01-01&api_key=lxFg4mPZkaDYsADeWLV9KdiZQds7T9A8zVih7Yuk').then(response => console.log(response))
    }
  }
}
</script>

<style lang="scss">
@import 'assets/fonts.css';
@import 'scss/reset.scss';

:root {
  --Black: #000;
  --Orange-Base: #F86600;
  --White-Base: #FFF;
}

.wrapper {
  widows: 100%;
  min-height: 100vh;
  background-color: var(--Black);
}

.header {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
}

.header__title {
  font-family: Passion One;
  font-size: 32px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
  color: var(--Orange-Base);
}

.header__text {
  color: var(--White-Base);
  font-family: Helvetica;
  font-size: 16px;
  font-style: normal;
  font-weight: 400;
  line-height: 24px;
}

.basket {
  position: fixed;
  bottom: 0;
  left: 0;
  right: 0;
  padding: 16px;
  background-color: #232526;
  display: flex;
  justify-content: space-between;
  align-items: center;
  color: #FFF;
  font-family: Helvetica;
  font-size: 16px;
  font-style: normal;
  font-weight: 400;
  line-height: 24px;

  &__title{
    font-size: 18px;
    font-style: normal;
    font-weight: 700;
  }
  &__button{
    padding: 12px 16px;
    border-radius: 40px;
    background:  #F86600;
  }
}
</style>

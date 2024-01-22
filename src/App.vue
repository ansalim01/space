<template>
  <div class="wrapper">
    <div class="content">
      <header class="header">
        <div class="header__title">
          ARMAGEDDON 2023
        </div>
        <div class="header__text">ООО “Команда им. Б. Уиллиса”. Взрываем астероиды с 1998 года.</div>
      </header>
      <main class="main">
        <div class="main__title">Ближайшие подлёты астероидов</div>
        <div class="main__toggle">
          <span class="main__toggle-not-active">в километрах</span> |
          <span class="main__toggle-active">в лунных орбитах</span>
        </div>
        <div class="main__row">
          <div class="row__items">
            <div class="item">
              <div class="item__title">12 сент 2023</div>
              <div class="item__info">
                <div class="item__distance">
                  <div class="item__distance-text">3 лунные орбиты</div>
                  <div class="item__distance-arr">
                    <svg xmlns="http://www.w3.org/2000/svg" width="129" height="6" viewBox="0 0 129 6" fill="none">
                      <path d="M0 3L5 5.88675L5 0.113249L0 3ZM129 3.00001L124 0.113259L124 5.88676L129 3.00001ZM4.5 3.5L124.5 3.50001L124.5 2.50001L4.5 2.5L4.5 3.5Z" fill="white" fill-opacity="0.5"/>
                    </svg>
                  </div>
                </div>
                <div class="item__img">
                  <img src="./assets/pngegg 2.png">
                </div>
                <div class="item__size">
                  2024FQ
                </div>
              </div>
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
  <div class="bg-img">
    <img src="./assets/earth.jpeg" alt="">
  </div>
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
.bg-img{
  position: fixed;
  width: 377px;
  height: 436px;
  top: calc(50% - 436px / 2);
  left: - 377px / 1.7;
  z-index: 0;
  img{
    width: 100%;
    height: 100%;
  }
}
.wrapper{
  widows: 100%;
  min-height: 100vh;
  background-color: var(--Black);
  padding: 16px;
}

.content{
  position: relative;
  z-index: 1;
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
.main{
padding: 17px 8px 0 56px;
}

.main__title{
  color: var(--White-Base);
font-family: Helvetica;
font-size: 28px;
font-style: normal;
font-weight: 700;
line-height: 36px; /* 128.571% */
}

.main__toggle{
  color: var(--White-Base);
  font-family: Helvetica;
  font-size: 16px;
  font-style: normal;
  font-weight: 400;
  line-height: 24px; /* 150% */
  &-active{
    font-weight: 700;
  }
  &-not-active{
    text-decoration-line: underline;
  }
}

.item{
  &__title{
    color: var(--White-Base);

    font-family: Helvetica;
    font-size: 24px;
    font-style: normal;
    font-weight: 700;
    line-height: 32px; /* 133.333% */
  }

  &__info{
    display: flex;
    justify-content: space-between;
  }

    &__distance{
      &-text{
        color: var(--White-Base);
        text-align: center;
        font-family: Helvetica;
        font-size: 16px;
        font-style: normal;
        font-weight: 400;
        line-height: 24px; /* 150% */
      }
    }
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

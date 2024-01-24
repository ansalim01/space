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
                <div class="item__right">
                  <div class="item__right-title">2024FQ</div>
                  <div class="item__right-size">Ø 85 м</div>
                </div>
              </div>
              <div class="item__bottom">
                <div class="item__bottom-button">заказать</div>
                <div class="item__bottom-warning">
                  <svg width="13px" height="13px" viewBox="0 0 512 512" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" aria-hidden="true" role="img" class="iconify iconify--fxemoji" preserveAspectRatio="xMidYMid meet">
                    <path fill="#FFB636" d="M12.51 470.379L234.371 16.008c6.439-13.187 25.17-13.363 31.855-.299l232.51 454.371c6.064 11.849-2.542 25.92-15.853 25.92H28.512c-13.164 0-21.778-13.791-16.002-25.621z"></path>
                    <path fill="#2B3B47" d="M284.332 173L272.15 336.498c-.911 12.233-11.567 21.411-23.8 20.499c-11.116-.828-19.706-9.707-20.499-20.499L215.668 173c-1.413-18.961 12.813-35.478 31.774-36.89s35.478 12.813 36.89 31.774c.124 1.662.109 3.5 0 5.116zM250 391.873c-17.432 0-31.564 14.131-31.564 31.564C218.436 440.869 232.568 455 250 455s31.564-14.131 31.564-31.564c0-17.432-14.132-31.563-31.564-31.563z"></path>
                  </svg>
                  Опасен
                </div>
              </div>
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
  --Orange-Smooth: rgba(248, 102, 0, 0.15);
  --gray-30: #E3E5E5;
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
  padding: 16px 16px 96px 16px;

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
  font-family: Helvetica;
  font-size: 28px;
  font-style: normal;
  font-weight: 700;
  line-height: 36px; /* 128.571% */
}

.main__toggle{

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
        text-align: center;
        font-size: 16px;
        font-weight: 400;
        line-height: 24px; /* 150% */
      }
  }
  &__right {
    // display: flex;
    &-title {
      font-size: 16px;
      font-weight: 700;
      line-height: 24px; /* 150% */
      text-decoration-line: underline;
    }
    &-size {
      font-size: 12px;
      font-weight: 400;
      line-height: 16px; /* 133.333% */
    }
  }
&__bottom{
  display: flex;
  gap: 10px;
  &-button {
    display: inline-flex;
    justify-content: center;
    align-items: center;
    padding: 2px 11px;
    border-radius: 16px;
    background: var(--Orange-Smooth);

    color: var(--Orange-Base);
    font-size: 11px;
    font-weight: 700;
    line-height: 20px; /* 181.818% */
  }

  &-warning {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 4px;
    color: var(--gray-30);
    font-size: 14px;
    font-weight: 400;
    line-height: 20px; /* 142.857% */
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

<template>
  <div class="tariff">
    <div class="container">
      <a href="#" class="tariff__link"> Тарифные планы</a>
      <h2 class="tariff__title">Какие у нас тарифные планы?</h2>
      <p class="tariff__desc">Цена на отправку одного документа</p>
      <input type="radio" name="testimonial" id="t-1" />
      <input type="radio" name="testimonial" id="t-2" checked />
      <input type="radio" name="testimonial" id="t-3" />

      <div class="tariff__testimonials">
        <label class="tariff__item" for="t-1">
          <h3 class="tariff__testimonials-title">Бизнес 500</h3>
          <p class="tariff__testimonials-money">345 сум</p>
          <p class="tariff__desc">
            Тариф для пользователей отправляющих до 500 (пятисот) документов в
            месяц
          </p>
          <second-button class="tariff__btn" v-text="ButtonName">
          </second-button>
        </label>
        <label class="tariff__item" for="t-2">
          <h3 class="tariff__testimonials-title">Старт</h3>
          <p class="tariff__testimonials-money">506 сум</p>
          <p class="tariff__desc">
            Тариф для пользователей отправляющих до 500 (пятисот) документов в
            месяц
          </p>
          <second-button class="tariff__btn" v-text="ButtonName">
          </second-button>
        </label>
        <label class="tariff__item" for="t-3">
          <h3 class="tariff__testimonials-title">Бизнес 1000</h3>
          <p class="tariff__testimonials-money">276 сум</p>
          <p class="tariff__desc">
            Тариф для пользователей отправляющих до 500 (пятисот) документов в
            месяц
          </p>
          <second-button class="tariff__btn" v-text="ButtonName">
          </second-button>
        </label>
      </div>
      <div class="dots">
        <label for="t-1"></label>
        <label for="t-2"></label>
        <label for="t-3"></label>
      </div>
    </div>
  </div>
</template>

<script>
import SecondButton from "@/./components/invoiceLandingPage/UiElements/OneButton.vue";
export default {
  data() {
    return {
      ButtonName: "Оформить",
    };
  },
  components: {
    SecondButton,
  },
};
</script>

<style lang="scss" scoped>
@import "@/./style/veraibles.scss";
.tariff__title {
  font-size: 64px;
  line-height: 78px;
  text-align: center;
}
.tariff__link {
  display: block;
  font-size: 40px;
  line-height: 49px;
  color: $colorMain;
  text-align: center;
}
.tariff__desc {
  font-size: 40px;
  line-height: 49px;
  color: #000000;
  opacity: 0.87;
  text-align: center;
}
.tariff {
  margin-top: 150px;
  width: 100%;
}
.tariff input {
  display: none;
}
.tariff__testimonials {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  position: relative;
  min-height: 700px;
  perspective: 1000px;
  overflow: hidden;
}
.tariff__testimonials-title {
  margin-top: 100px;
  margin-bottom: 43px;
  font-size: 40px;
  line-height: 49px;
}
.tariff__desc {
  margin-bottom: 100px;
  font-size: 24px;
  line-height: 29px;
  text-align: center;
}
.tariff__testimonials-money {
  font-size: 48px;
  line-height: 78px;
}
.tariff__btn {
  margin-bottom: 100px;
}
.tariff__item {
  top: 0;
  position: absolute;
  box-sizing: border-box;
  background-color: #fff;
  padding: 30px;
  width: 450px;
  text-align: center;
  transition: transform 0.4s;
  -webkit-transform-style: preserve-3d;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.3);
  user-select: none;
  cursor: pointer;
}
.tariff__testimonials .tariff__item {
  width: 500px;
  height: 600px;
  border-radius: 25px;
}

.dots {
  display: flex;
  justify-content: center;
  align-items: center;
}
.dots label {
  display: block;
  height: 5px;
  width: 5px;
  border-radius: 50%;
  cursor: pointer;
  background-color: #413b52;
  margin: 7px;
  transition: transform 0.2s, color 0.2s;
}
/* First */
#t-1:checked ~ .dots label[for="t-1"] {
  transform: scale(2);
  background-color: #413b52;
}
#t-1:checked ~ .dots label[for="t-2"] {
  transform: scale(1.5);
}
#t-1:checked ~ .tariff__testimonials label[for="t-1"] {
  z-index: 4;
  background-color: $colorMain;
  color: #fff;
}
#t-1:checked ~ .tariff__testimonials label[for="t-2"] {
  transform: translateX(300px) translateZ(-90px) rotateY(-15deg);
  z-index: 3;
  .tariff__btn {
    display: none;
  }
}
#t-1:checked ~ .tariff__testimonials label[for="t-3"] {
  transform: translateX(600px) translateZ(-180px) rotateY(-25deg);
  z-index: 2;
  .tariff__btn {
    display: none;
  }
}

/* Second */
#t-2:checked ~ .dots label[for="t-1"] {
  transform: scale(1.5);
}
#t-2:checked ~ .dots label[for="t-2"] {
  transform: scale(2);
  background-color: #413b52;
}
#t-2:checked ~ .dots label[for="t-3"] {
  transform: scale(1.5);
}
#t-2:checked ~ .tariff__testimonials label[for="t-1"] {
  transform: translateX(-300px) translateZ(-90px) rotateY(15deg);
  .tariff__btn {
    display: none;
  }
}
#t-2:checked ~ .tariff__testimonials label[for="t-2"] {
  z-index: 3;
  color: #fff;
  background-color: $colorMain;
}
#t-2:checked ~ .tariff__testimonials label[for="t-3"] {
  transform: translateX(300px) translateZ(-90px) rotateY(-15deg);

  z-index: 2;
  .tariff__btn {
    display: none;
  }
}

/* Third */
#t-3:checked ~ .dots label[for="t-2"] {
  transform: scale(1.5);
}
#t-3:checked ~ .dots label[for="t-3"] {
  transform: scale(2);
  background-color: #413b52;
}
#t-3:checked ~ .dots label[for="t-4"] {
  transform: scale(1.5);
}
#t-3:checked ~ .tariff__testimonials label[for="t-1"] {
  transform: translateX(-600px) translateZ(-180px) rotateY(25deg);
  .tariff__btn {
    display: none;
  }
}
#t-3:checked ~ .tariff__testimonials label[for="t-2"] {
  transform: translateX(-300px) translateZ(-90px) rotateY(15deg);
  .tariff__btn {
    display: none;
  }
}
#t-3:checked ~ .tariff__testimonials label[for="t-3"] {
  background-color: $colorMain;
  color: #fff;
  z-index: 3;
}
@media screen and (max-width: 1098px) {
}
</style>

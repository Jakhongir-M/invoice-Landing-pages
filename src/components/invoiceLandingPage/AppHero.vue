<template>
  <div class="hero">
    <div class="container">
      <div class="hero__box">
        <div class="hero__left">
          <h1 class="hero__left-title">
            E-invoce-Интерактивная платформа для обеспечения электронного
            документооборота и обработки данных
          </h1>
          <div class="hero__left-box">
            <app-button class="hero__btn">Узнать подробнее</app-button>
          </div>
        </div>
        <div class="hero__right">
          <img src="@/./assets/img/hero-Landing/photo-hero.png" alt="" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import AppButton from "@/./components/invoiceLandingPage/UiElements/SecondButton.vue";
export default {
  data() {
    return {
      HeroNameButton: "Узнать подробнее",
    };
  },
  components: {
    AppButton,
  },
};
</script>

<style scoped lang="scss">
@import "@/./style/veraibles.scss";
.hero {
  padding-top: 100px;
  .container {
    max-width: 1580px;
    margin: 0px auto;
    padding: 0px 60px;
  }
  .hero__box {
    display: flex;
    justify-content: space-between;
  }
  .hero__left {
    max-width: 960px;
  }
  .hero__left-title {
    font-size: 63px;
    line-height: 65px;
    color: #000000;
    opacity: 0.87;
    margin-top: 20px;
    margin: 0px;
    margin-bottom: 50px;
  }

  .hero__left-video {
    width: 75px;
    height: 75px;
  }
  .hero__left-img {
    color: $colorMain;
  }

  .hero__left-link {
    color: #fff;
    padding: 18px 38px;
    background-color: $colorMain;
    border-radius: 50px;
    font-size: 22px;
    line-height: 27px;
  }

  .hero__right {
    width: 600px;
    height: 550px;
    border-radius: 55px;
  }
  @media screen and (max-width: 1600px) {
    .hero {
      padding-top: 100px;
    }
    .hero__left-title {
      font-size: 50px;
    }
    .hero__left {
      max-width: 800px;
    }
    .hero__right {
      width: 500px;
    }
    .hero__box {
    }
  }
  @media screen and (max-width: 1400px) {
    .hero__left-title {
      font-size: 55px;
      line-height: 60px;
    }
    .hero__left {
      max-width: 650px;
    }
    .hero__right {
      width: 400px;
      height: 400px;
    }
    .hero__box {
    }
  }
  @media screen and (max-width: 1200px) {
    .hero__left-title {
      font-size: 40px;
      line-height: 50px;
    }
    .hero__left {
      max-width: 550px;
    }
    .hero__right {
      width: 350px;
      height: 350px;
    }
  }
  @media screen and (max-width: 1000px) {
    .hero__left-title {
      font-size: 30px;
      line-height: 40px;
      margin-bottom: 10px;
    }
    .hero__left {
      max-width: 400px;
    }
    .hero__right {
      width: 300px;
      height: 300px;
    }
    .hero__btn {
      font-size: 15px;
      padding: 10px 10px;
    }
  }
  @media screen and (max-width: 820px) {
    .hero__left-title {
      font-size: 25px;
      line-height: 30px;
      margin-bottom: 30px;
    }
    .hero__left {
      max-width: 400px;
    }
    .hero__right {
      width: 250px;
      height: 250px;
    }
    .hero__btn {
      font-size: 20px;
      padding: 20px 20px;
      margin-bottom: 20px;
    }
  }
  @media screen and (max-width: 750px) {
    .hero__left-title {
      font-size: 35px;
      line-height: 40px;
      margin-bottom: 30px;
    }
    .hero__left {
      max-width: 500px;
      text-align: center;
    }
    .hero__right {
      width: 350px;
      height: 350px;
    }
    .hero__btn {
      font-size: 20px;
      padding: 20px 20px;
      margin-bottom: 20px;
    }
    .hero__box {
      flex-direction: column;
      align-items: center;
    }
  }
  @media screen and (max-width: 570px) {
    .hero__left-title {
      font-size: 40px;
      line-height: 40px;
      margin-bottom: 20px;
    }
    .hero__left {
      max-width: 400px;
      text-align: center;
    }

    .hero__btn {
      font-size: 20px;
      padding: 20px 20px;
      margin-bottom: 20px;
    }
    .hero__box {
      flex-direction: column;
      align-items: center;
    }
    .container {
      padding: 0px 20px;
    }
  }
  @media screen and (max-width: 420px) {
    .hero__left-title {
      font-size: 30px;
      line-height: 40px;
      margin-bottom: 20px;
    }
    .hero__left {
      max-width: 400px;
      text-align: center;
    }
    .hero__right {
      width: 300px;
      height: 300px;
    }
    .hero__btn {
      margin-bottom: 20px;
    }
    .hero {
      padding-top: 50px;
    }
  }
}
</style>

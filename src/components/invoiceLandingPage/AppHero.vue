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
            <app-button>Узнать подробнее</app-button>
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
}
</style>

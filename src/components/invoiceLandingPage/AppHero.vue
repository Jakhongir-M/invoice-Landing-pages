<template>
  <div class="hero">
    <div class="container">
      <div class="hero__box">
        <div class="hero__left">
          <h1 class="hero__title">
            Инвойс — в международной коммерческой практике документ
          </h1>
          <div class="hero__left-box">
            <a class="hero__info" href="">Узнать подробнее</a>
            <a class="hero__video" href=""
              ><img
                class="hero__video-img"
                src="@/./assets/img/hero-Landing/Play.svg"
                alt=""
            /></a>
            <a class="hero__start" href="">Начать работу</a>
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
export default {};
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
    max-width: 710px;
  }
  .hero__right {
  }
  .hero__left-box {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .hero__info {
    color: #fff;
    padding: 18px 38px;
    background-color: $colorMain;
    font-size: 22px;
    line-height: 27px;
    border-radius: 50px;
  }
  .hero__video {
    width: 75px;
    height: 75px;
  }
  .hero__video-img {
    width: 75px;
    height: 75px;
  }
  .hero__start {
    color: #fff;
    padding: 18px 38px;
    background-color: $colorMain;
    border-radius: 50px;
    font-size: 22px;
    line-height: 27px;
  }
  .hero__title {
    font-size: 64px;
    line-height: 78px;
    color: #000000;
    opacity: 0.87;
  }
  .hero__right {
    width: 600px;
    height: 550px;
    border-radius: 55px;
  }
}
</style>

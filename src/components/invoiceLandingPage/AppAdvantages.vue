<template>
  <div class="advantages">
    <div class="container">
      <div class="advantages__box">
        <div class="advantages__left">
          <a href="#" class="advantages__link">О сервисе</a>
          <h2 class="advantages__title">Основные преимущества сервиса</h2>
          <p class="advantages__desc">
            Справа перечисленны основные преимущества сервиса E-invoice
          </p>
        </div>
        <div class="advantages__right">
          <ul class="advantages__list list">
            <li class="list__item">
              <img
                class="list__img"
                src="@/./assets/img/advantages-Landing/Icon-1.svg"
                alt=""
              />
              <h3 class="list__title">Удобность</h3>
              <p class="list__desc">
                Сервис Удобный и Комфортный для пользования
              </p>
            </li>
            <li class="list__item">
              <img
                class="list__img"
                src="@/./assets/img/advantages-Landing/Icon-3.svg"
                alt=""
              />
              <h3 class="list__title">Скорость работы</h3>
              <p class="list__desc">
                Ваши документ будут обработаны в кратчайшие сроки
              </p>
            </li>
            <li class="list__item">
              <img
                class="list__img"
                src="@/./assets/img/advantages-Landing/Icon-2.svg"
                alt=""
              />
              <h3 class="list__title">Безопасноть</h3>
              <p class="list__desc">
                Ваши данные будут Конфиденциальны и доступны только вам
              </p>
            </li>
            <li class="list__item">
              <img
                class="list__img"
                src="@/./assets/img/advantages-Landing/Icon-4.svg"
                alt=""
              />
              <h3 class="list__title">Обратная связь</h3>
              <p class="list__desc">
                Служба поддержки готова ответить в любой момент
              </p>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import gsap from "gsap";
export default {
  mounted() {
    gsap.from(
      ".advantages__left, .advantages__link, .advantages__title, .advantages__desc",
      {
        scale: 0.2,
        opacity: 0,
        stagger: 0.2,
        rotation: 0,
        y: 100,
        duration: 0.5,
        scrollTrigger: {
          start: "0 100%",
          trigger:
            "advantages__left, .advantages__link, .advantages__title, .advantages__desc",
          toggleActions: "play none none none",
        },
      }
    );
    gsap.from(".list__item", {
      scale: 0.5,
      opacity: 0,
      stagger: 0.2,
      rotation: 0,
      y: 200,
      duration: 0.5,
      scrollTrigger: {
        start: "0px 100%",
        trigger: ".list__item",
        toggleActions: "play none none none",
      },
    });
  },
};
</script>

<style scoped lang="scss">
@import "@/./style/veraibles.scss";
.advantages {
  padding-top: 50px;
  // .advantages__box

  &__box {
    display: flex;
    align-items: center;
  }

  // .advantages__left

  &__left {
    min-width: 820px;
  }

  // .advantages__link

  &__link {
    font-size: 40px;
    line-height: 49px;
    color: $colorMain;
  }

  // .advantages__title

  &__title {
    font-size: 60px;
    line-height: 78px;
  }

  // .advantages__desc

  &__desc {
    font-size: 35px;
    line-height: 49px;
    opacity: 0.87;
  }
  &__right {
  }

  &__list {
  }
}
.list {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;

  &__item {
    margin: 5px;
    padding: 30px 40px;
    width: 300px;
    height: 350px;
    display: flex;
    flex-direction: column;
    align-items: center;
    background: #ffffff;
    box-shadow: 0px 0px 15px rgba(0, 0, 0, 0.075);
    border-radius: 25px;
  }
  &__item:nth-child(1) {
    margin-top: 60px;
  }
  &__item:nth-child(3) {
    margin-top: 60px;
  }

  // .list__img

  &__img {
    margin-bottom: 30px;
    width: 125px;
    height: 125px;
  }

  // .list__title

  &__title {
    margin-bottom: 24px;
    font-size: 23px;
    line-height: 29px;
    color: #000000;
    opacity: 0.87;
  }

  // .list__desc

  &__desc {
    font-size: 20px;
    line-height: 24px;
    text-align: center;
    color: #000000;
    opacity: 0.75;
  }
}

@media screen and (max-width: 1530px) {
  .list__item {
    width: 200px;
    height: 300px;
  }
  .list__title {
    font-size: 20px;
    line-height: 20px;
    margin-bottom: 15px;
    text-align: center;
  }
  .list__desc {
    font-size: 15px;
    line-height: 18px;
  }
  .advantages__box {
  }
  .advantages__left {
    min-width: 300px;
  }
  .advantages__link {
    font-size: 35px;
    line-height: 40px;
  }
  .advantages__title {
    font-size: 50px;
    line-height: 70px;
  }
  .advantages__desc {
  }
  .list__img {
    width: 90px;
    height: 90px;
    margin-bottom: 10px;
  }
}

@media screen and (max-width: 1150px) {
  .advantages__box {
    display: flex;
    flex-direction: column;
  }
  .list__item:nth-child(1) {
    margin-top: 0px;
  }
  .list__item:nth-child(3) {
    margin-top: 0px;
  }
  .advantages__left {
    margin-bottom: 50px;
    text-align: center;
  }

  .advantages__title {
    font-size: 40px;
    line-height: 70px;
    margin-bottom: 10px;
  }
  .advantages__desc {
    font-size: 30px;
  }
  .advantages__list {
    align-items: center;
  }
}
@media screen and (max-width: 1150px) {
  .advantages__title {
    font-size: 30px;
    line-height: 40px;
    margin-bottom: 10px;
  }
  .advantages__desc {
    font-size: 20px;
    line-height: 25px;
  }
  .advantages__link {
    font-size: 25px;
    line-height: 40px;
  }
  .list {
    flex-wrap: wrap;
    justify-content: center;
  }
  .list__item {
    width: 400px;
    height: 400px;
  }
  .list__title {
    font-size: 30px;
    line-height: 20px;
    margin-bottom: 15px;
    text-align: center;
  }
  .list__img {
    width: 150px;
    height: 150px;
    margin-bottom: 20px;
  }
  .list__desc {
    font-size: 20px;
    line-height: 40px;
  }
}
@media screen and (max-width: 900px) {
  .list {
    flex-wrap: wrap;
    justify-content: center;
  }
  .list__item {
    width: 250px;
    height: 350px;
  }
  .list__title {
    font-size: 25px;
    line-height: 25px;
    margin-bottom: 15px;
    text-align: center;
  }
  .list__img {
    width: 100px;
    height: 100px;
    margin-bottom: 20px;
  }
  .list__desc {
    font-size: 18px;
    line-height: 25px;
  }
}
@media screen and (max-width: 585px) {
  .list {
    flex-wrap: wrap;
    justify-content: center;
  }
  .list__item {
    width: 300px;
    height: 300px;
  }
  .list__title {
    font-size: 30px;
    line-height: 30px;
    margin-bottom: 15px;
    text-align: center;
  }
  .advantages__title {
    font-size: 35px;
    line-height: 40px;
    margin-bottom: 10px;
  }
  .advantages__desc {
    font-size: 20px;
    line-height: 25px;
  }
  .advantages__link {
    font-size: 25px;
    line-height: 40px;
  }
}
</style>

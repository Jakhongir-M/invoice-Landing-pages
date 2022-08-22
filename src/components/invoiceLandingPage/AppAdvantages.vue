<template>
  <div class="advantages">
    <div class="container">
      <div class="advantages__box">
        <div class="advantages__left">
          <a href="" class="advantages__link">О сервисе</a>
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
              <h3 class="list__title">Доступность</h3>
              <p class="list__desc">Сервис доступен для всех, всего и вся</p>
            </li>
            <li class="list__item">
              <img
                class="list__img"
                src="@/./assets/img/advantages-Landing/Icon-3.svg"
                alt=""
              />
              <h3 class="list__title">Скорость работы</h3>
              <p class="list__desc">Сервис доступен для всех, всего и вся</p>
            </li>
            <li class="list__item">
              <img
                class="list__img"
                src="@/./assets/img/advantages-Landing/Icon-2.svg"
                alt=""
              />
              <h3 class="list__title">Безопасноть</h3>
              <p class="list__desc">Сервис доступен для всех, всего и вся</p>
            </li>
            <li class="list__item">
              <img
                class="list__img"
                src="@/./assets/img/advantages-Landing/Icon-4.svg"
                alt=""
              />
              <h3 class="list__title">Обратная связь</h3>
              <p class="list__desc">Сервис доступен для всех, всего и вся</p>
            </li>
          </ul>
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
</style>

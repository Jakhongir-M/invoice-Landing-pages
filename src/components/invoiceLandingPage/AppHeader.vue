<template>
  <header class="header">
    <div class="container">
      <div class="header__box">
        <a class="header__logo" href=""
          ><img src="@/./assets/img/header-Landing/Logo.svg" alt=""
        /></a>
        <nav class="header__nav">
          <ul class="header__list-nav">
            <li class="header__list-item">
              <a class="header__nav-link" href="#">Главная</a>
            </li>
            <li class="header__list-item">
              <a class="header__nav-link" href="#">Контакты</a>
            </li>
            <li class="header__list-item">
              <a class="header__nav-link" href="#">Информация</a>
            </li>
            <a class="header__list-btn" href="#">Авторизоваться</a>
          </ul>
        </nav>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  data() {
    return {
      items: ["Home", "about", "blog"],
      show: false,
    };
  },
};
</script>

<style scoped lang="scss">
@import "@/./style/veraibles.scss";

.header {
  .header__nav-mobile {
    display: none;
  }
  .header__box {
    padding: 40px 0px;
  }
  .header__box {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .header__logo {
    width: 120px;
    height: 75px;
  }
  .header__nav {
    display: flex;
    align-items: center;
  }
  .header__list-nav {
    display: flex;
    align-items: center;
  }

  .header__list-item {
    margin-right: 50px;
  }
  &__list-item:nth-child(3) {
    margin-right: 100px;
  }
  .header__nav-link {
    color: #000000;
    opacity: 0.5;
    font-size: 24px;
    line-height: 29px;
    letter-spacing: 0.03em;
  }
  .header__nav-link:hover {
    border-bottom: solid 3px $colorMain;
  }
  .header__nav-link:active {
    color: $colorMain;
  }
  .header__list-btn {
    color: #fff;
    padding: 18px 38px;
    background-color: $colorMain;
    border-radius: 15px;
    font-size: 20px;
    line-height: 24px;
  }
  &__list-btn:hover {
    opacity: 0.9;
  }
  &__list-btn:active {
    opacity: 0.5;
  }
  @media screen and (max-width: 1200px) {
    .header__nav-link {
      font-size: 15px;
      line-height: 20px;
    }
    .header__list-btn {
      font-size: 15px;
      line-height: 20px;
    }
  }
  @media screen and (max-width: 950px) {
    .header__nav {
      display: none;
    }
    .header__nav-mobile {
      display: block;
    }
  }
}
</style>

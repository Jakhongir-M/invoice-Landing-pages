<template>
  <!-- Hamburger -->
  <nav role="navigation">
    <div id="menuToggle">
      <input type="checkbox" />

      <span></span>
      <span></span>
      <span></span>

      <ul id="menu">
        <a href="#"><li>Home</li></a>
        <a href="#"><li>About</li></a>
        <a href="#"><li>Info</li></a>
        <a href="#"><li>Contact</li></a>
        <a href="https://erikterwan.com/" target="_blank"
          ><li>Show me more</li></a
        >
      </ul>
    </div>
  </nav>
  <!-- hamburger FINISHED -->
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
              <a class="header__nav-link" href="#">Информация</a>
            </li>
            <li class="header__list-item">
              <a class="header__nav-link" href="#">Контакты</a>
            </li>
            <li class="header__list-item">
              <a class="header__nav-link" href="#">Тарифы</a>
            </li>
            <li class="header__list-item">
              <a class="header__nav-link" href="#">Клиенты</a>
            </li>
            <li>
              <app-button v-text="buttontext"></app-button>
            </li>
          </ul>
        </nav>
      </div>
    </div>
  </header>
</template>

<script>
import AppButton from "@/components/invoiceLandingPage/UiElements/OneButton.vue";
export default {
  data() {
    return {
      buttontext: "Авторизоваться",
      items: ["Home", "about", "blog"],
      show: false,
    };
  },
  components: {
    AppButton,
  },
};
</script>

<style scoped lang="scss">
@import "@/./style/veraibles.scss";
// BTN__________________________________________
#menuToggle {
  display: none;
  position: relative;
  top: 50px;
  left: 50px;
  z-index: 1;
  -webkit-user-select: none;
  user-select: none;
  text-align: left;
}

#menuToggle a {
  text-decoration: none;
  color: #232323;
  transition: color 0.3s ease;
}

#menuToggle a:hover {
  color: tomato;
}

#menuToggle input {
  display: block;
  width: 40px;
  height: 32px;
  position: absolute;
  top: -7px;
  left: -5px;

  cursor: pointer;

  opacity: 0; /* hide this */
  z-index: 2; /* and place it over the hamburger */

  -webkit-touch-callout: none;
}

/*
 * Just a quick hamburger
 */
#menuToggle span {
  display: block;
  width: 33px;
  height: 4px;
  margin-bottom: 5px;
  position: relative;

  background: #cdcdcd;
  border-radius: 3px;

  z-index: 1;

  transform-origin: 4px 0px;

  transition: transform 0.5s cubic-bezier(0.77, 0.2, 0.05, 1),
    background 0.5s cubic-bezier(0.77, 0.2, 0.05, 1), opacity 0.55s ease;
}

#menuToggle span:first-child {
  transform-origin: 0% 0%;
}

#menuToggle span:nth-last-child(2) {
  transform-origin: 0% 100%;
}

#menuToggle input:checked ~ span {
  opacity: 1;
  transform: rotate(45deg) translate(-2px, -1px);
  background: #232323;
}

#menuToggle input:checked ~ span:nth-last-child(3) {
  opacity: 0;
  transform: rotate(0deg) scale(0.2, 0.2);
}

#menuToggle input:checked ~ span:nth-last-child(2) {
  transform: rotate(-45deg) translate(0, -1px);
}

#menu {
  position: absolute;
  width: 50%;
  margin: -100px 0 0 -50px;
  padding: 50px;
  padding-top: 125px;

  background: #ededed;
  list-style-type: none;
  -webkit-font-smoothing: antialiased;
  transform-origin: 0% 0%;
  transform: translate(-100%, 0);
  transition: transform 0.5s cubic-bezier(0.77, 0.2, 0.05, 1);
}
#menu li {
  padding: 10px 0;
  font-size: 22px;
}

#menuToggle input:checked ~ ul {
  transform: none;
}

@media screen and (max-width: 1098px) {
  #menuToggle,
  span {
    display: block;
  }
  .header__box {
    justify-content: flex-end;
  }
}
// BTN FINISHED___________________________________
.header {
  background-color: $colorMain;
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
    margin-right: 30px;
  }
  &__list-item:nth-child(5) {
    margin-right: 100px;
  }
  // _____________________________________________________________________________
  // LINK HOVER
  .header__nav-link {
    position: relative;
    font-size: 24px;
    line-height: 29px;
    letter-spacing: 0.03em;

    color: #ffffff;
  }

  .header__nav-link::before {
    content: "";
    position: absolute;
    bottom: -3px;
    right: 0;
    width: 0;
    height: 3px;
    background-color: #fff;
    transition: width 0.6s cubic-bezier(0.25, 1, 0.5, 1);
  }

  @media (hover: hover) and (pointer: fine) {
    .header__nav-link:hover::before {
      left: 0;
      right: auto;
      width: 100%;
    }
  }
  // LINK HOVER FINISHED
  // ___________________________________________________________________________________
  // BTN START

  // BTN FINISH

  @media screen and (max-width: 1200px) {
    .header__nav-link {
      font-size: 15px;
      line-height: 20px;
    }
    .header__list-btn {
      font-size: 15px;
      line-height: 20px;
      border: 2px solid #ffffff;
    }
  }
  @media screen and (max-width: 1098px) {
    .header__nav {
      display: none;
    }
    .header__nav-mobile {
      display: block;
    }
  }
}
</style>

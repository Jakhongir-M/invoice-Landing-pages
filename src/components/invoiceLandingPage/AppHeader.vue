<template>
  <header class="header">
    <div class="container">
      <!-- Hamburger -->
      <nav role="navigation">
        <div id="hamburger__menuToggle">
          <input type="checkbox" />

          <span></span>
          <span></span>
          <span></span>

          <ul id="menu">
            <a href="#"><li>Главная</li></a>
            <a href="#"><li>Информация</li></a>
            <a href="#"><li>Контакты</li></a>
            <a href="#"><li>Тарифы</li></a>
            <li><a href="#clients">Клиенты</a></li>
          </ul>
        </div>
      </nav>
      <!-- hamburger FINISHED -->

      <div class="header__box">
        <a class="header__logo" href=""
          ><img src="@/./assets/img/header-Landing/Logo.svg" alt=""
        /></a>
        <nav class="header__nav">
          <ul class="header__list-nav">
            <li class="header__list-item">
              <a class="header__nav-link" id="header" href="#">Главная</a>
            </li>
            <li class="header__list-item">
              <a class="header__nav-link" href="#">Информация</a>
            </li>
            <li class="header__list-item">
              <a class="header__nav-link" href="#">Контакты</a>
            </li>
            <li class="header__list-item">
              <a class="header__nav-link" href="#tariff">Тарифы</a>
            </li>
            <li class="header__list-item">
              <a class="header__nav-link" href="#clients">Клиенты</a>
            </li>
            <li class="header__list-item">
              <app-button class="header__btn">Авторизоваться</app-button>
            </li>
          </ul>
        </nav>
      </div>
    </div>
  </header>
</template>

<script>
import gsap from "gsap";
import AppButton from "@/components/invoiceLandingPage/UiElements/OneButton.vue";

export default {
  mounted() {
    gsap.from(".header__logo ", {
      scale: 0.5,
      opacity: 0,
      rotation: 0,
      x: 0,
      y: 200,
      duration: 0.5,
    });
    gsap.from(".header__list-item", {
      scale: 0.5,
      opacity: 0,
      stagger: 0.1,
      rotation: 0,
      x: 0,
      y: 150,
      duration: 1,
    });
  },
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
// // HAMBURGET START__________________________________________
#hamburger__menuToggle {
  display: none;
  position: relative;
  top: 50px;
  left: 0px;
  z-index: 1;
  -webkit-user-select: none;
  user-select: none;
  text-align: left;
}
#hamburger__menuToggle a {
  text-decoration: none;
  color: #232323;
  transition: color 0.3s ease;
}

#hamburger__menuToggle a:hover {
  color: $colorMain;
}

#hamburger__menuToggle input {
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
#hamburger__menuToggle span {
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

#hamburger__menuToggle span:first-child {
  transform-origin: 0% 0%;
}

#hamburger__menuToggle span:nth-last-child(2) {
  transform-origin: 0% 100%;
}

#hamburger__menuToggle input:checked ~ span {
  opacity: 1;
  transform: rotate(45deg) translate(-2px, -1px);
  background: #232323;
}

#hamburger__menuToggle input:checked ~ span:nth-last-child(3) {
  opacity: 0;
  transform: rotate(0deg) scale(0.2, 0.2);
}

#hamburger__menuToggle input:checked ~ span:nth-last-child(2) {
  transform: rotate(-45deg) translate(0, -1px);
}

#menu {
  position: absolute;
  width: 70%;
  margin: -125px 0 0 -50px;
  padding: 50px;
  padding-top: 150px;
  background: #ededed;
  list-style-type: none;
  -webkit-font-smoothing: antialiased;
  transform-origin: 0% 0%;
  transform: translate(-100%, 0);
  transition: transform 0.5s cubic-bezier(0.77, 0.2, 0.05, 1);
  border-radius: 50px;
}
#menu li {
  padding: 10px 0;
  font-size: 22px;
}

#hamburger__menuToggle input:checked ~ ul {
  transform: none;
}

// HAMBURGER___________________________________FINISHED

.header {
  background-color: $colorMain;
  .header__nav-mobile {
    display: none;
  }
  .header__box {
    padding: 40px 0px;
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

  // _________________________________Responsive______________________________________
  @media screen and (max-width: 1350px) {
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
    #hamburger__menuToggle {
      display: block;
    }
    .header__nav-mobile {
      display: block;
    }
    .header__box {
      justify-content: end;
    }
    .header__box {
      padding-bottom: 30px;
      padding-top: 0px;
    }
  }

  @media screen and (max-width: 380px) {
    #menu {
      width: 90%;
    }
  }
}
</style>

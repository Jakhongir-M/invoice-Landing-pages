<template>
  <div class="footer">
    <div class="container">
      <div class="footer__box">
        <a class="footer__logo" href=""
          ><img src="@/./assets/img/header-Landing/Logo.svg" alt=""
        /></a>
        <nav class="footer__nav">
          <ul class="footer__list-nav">
            <li class="footer__list-item">
              <a class="footer__nav-link" href="#header">На главную</a>
            </li>
            <li class="footer__list-item">
              <a class="footer__nav-link" href="#">О сервисе</a>
            </li>
            <li class="footer__list-item">
              <a class="footer__nav-link" href="#tariff">Тарифы</a>
            </li>
          </ul>
        </nav>
      </div>

      <hr />
      <div class="footer__contact">
        <div class="footer__contact-box">
          <a class="footer__contact-img" href="">
            <img src="@/./assets/img/footer-Landing/mail-1.svg" alt="" />
          </a>
          <h1 class="footer__contact-title">Почта</h1>
          <a class="footer__contact-link" href="einvoice.uz@gmail.com"
            >einvoice.uz@gmail.com</a
          >
        </div>
        <div class="footer__contact-box">
          <a class="footer__contact-img" href="">
            <img src="@/./assets/img/footer-Landing/phone-2.svg" alt="" />
          </a>
          <h1 class="footer__contact-title">Номер</h1>
          <a class="footer__contact-link" href="+998 71 200 03 30"
            >+998 71 200 03 30</a
          >
        </div>
        <div class="footer__contact-box">
          <a class="footer__contact-img" href="">
            <img src="@/./assets/img/footer-Landing/telegram-3.svg" alt="" />
          </a>
          <h1 class="footer__contact-title">Телеграм</h1>
          <a class="footer__contact-link" href="@Einvoice_bot">@Einvoice_bot</a>
        </div>
      </div>
      <hr />
      <div class="protection">
        <p>© e-invoice.uz 2022 г. Все права защищены</p>
      </div>
    </div>
  </div>
</template>

<script>
import gsap from "gsap";
export default {
  mounted() {
    gsap.from(
      ".footer__logo, .footer__nav-link, .footer__contact-img, .footer__contact-title",
      {
        scale: 0.5,
        opacity: 0,
        stagger: 0.2,
        rotation: 0,
        y: 200,
        duration: 0.7,
        scrollTrigger: {
          trigger:
            ".footer__logo, .footer__nav-link, .clients__title, .footer__contact-img, .footer__contact-title",
          toggleActions: "play none none none",
        },
      }
    );
  },
};
</script>

<style scoped lang="scss">
@import "@/./style/veraibles.scss";
.footer {
  margin-top: 150px;
  background-color: $colorMain;
  .header__nav-mobile {
    display: none;
  }
  .footer__box {
    padding: 40px 0px;
    display: flex;
    justify-content: start;
    align-items: center;
  }

  .footer__logo {
    width: 120px;
    height: 75px;
    margin-right: 200px;
  }
  .footer__nav {
    display: flex;
    align-items: center;
  }
  .footer__list-nav {
    display: flex;
    align-items: center;
  }

  .footer__list-item {
    margin-right: 30px;
  }

  .footer__contact {
    margin-top: 50px;
    margin-bottom: 50px;
    display: flex;
    justify-content: space-around;
    align-items: center;
  }

  // .footer__contact-img

  .footer__contact-img {
    width: 90px;
    height: 90px;
  }

  // .footer__contact-title

  .footer__contact-title {
  }

  // .footer__contact-link

  .footer__contact-link {
  }
  .footer__contact-box {
    display: flex;
    flex-direction: column;
    align-items: center;
    color: #fff;
  }
  .protection {
    text-align: start;
    color: #fff;
    padding-bottom: 50px;
    padding-top: 30px;
  }
  // _____________________________________________________________________________
  // LINK HOVER
  .footer__nav-link {
    position: relative;
    font-size: 24px;
    line-height: 29px;
    letter-spacing: 0.03em;

    color: #ffffff;
  }

  .footer__nav-link::before {
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
    .footer__nav-link:hover::before {
      left: 0;
      right: auto;
      width: 100%;
    }
  }
  @media screen and (max-width: 900px) {
    .footer__logo {
      margin-right: 100px;
    }
    .footer__nav-link {
      font-size: 25px;
      line-height: 40px;
    }
    .footer__list-nav {
      flex-direction: column;
      align-items: center;
      justify-content: center;
    }
    .footer__box {
      justify-content: space-between;
      align-items: center;
    }
    .footer__contact {
      flex-direction: column;
    }
    .footer__contact-box {
      margin-bottom: 50px;
    }
  }
  @media screen and (max-width: 500px) {
    .footer__logo {
      margin-right: 0px;
      margin-bottom: 50px;
    }
    .footer__nav-link {
      font-size: 20px;
      line-height: 40px;
    }
    .footer__box {
      flex-direction: column;
      align-items: center;
    }
    .footer__list-item {
      margin-right: 0px;
    }
  }
}
</style>

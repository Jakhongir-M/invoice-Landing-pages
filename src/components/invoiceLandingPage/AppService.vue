<template>
  <div class="service">
    <div class="_container">
      <div class="service__wrapper">
        <div class="service__box-desc">
          <p class="service__link" href="#">Инструкция</p>
          <h1 class="service__title">Как пользоваться сервисом?</h1>
          <p class="service__desc">
            Инструкция по отправке документов в налоговую через сервис E-invoice
          </p>
        </div>
        <div class="service__top">
          <ul class="service__list">
            <li
              class="service__item"
              ontouchstart="this.classList.toggle('hover');"
            >
              <div class="container">
                <div class="front service__front-1">
                  <div class="inner">
                    <p class="service__number">1</p>
                    <span class="service__text"
                      >Создайте необходимый документ</span
                    >
                  </div>
                </div>
                <div class="back">
                  <div class="inner">
                    <p>Войдите на сайт и создайте необходимый документ</p>
                  </div>
                </div>
              </div>
            </li>
            <li
              class="service__item"
              ontouchstart="this.classList.toggle('hover');"
            >
              <div class="container">
                <div class="front service__front-2">
                  <div class="inner">
                    <p class="service__number">2</p>
                    <span class="service__text">Выберите тип документа</span>
                  </div>
                </div>
                <div class="back">
                  <div class="inner">
                    <p>Выберите необходимый тип документа в разделе выбора</p>
                  </div>
                </div>
              </div>
            </li>
            <li
              class="service__item"
              ontouchstart="this.classList.toggle('hover');"
            >
              <div class="container">
                <div class="front service__front-3">
                  <div class="inner">
                    <p class="service__number">3</p>
                    <span class="service__text">Заполните документ</span>
                  </div>
                </div>
                <div class="back">
                  <div class="inner">
                    <p>Заполните все необходимые поля вашего Документа</p>
                  </div>
                </div>
              </div>
            </li>
            <li
              id="fron-4"
              class="service__item"
              ontouchstart="this.classList.toggle('hover');"
            >
              <div class="container">
                <div class="front service-front-4">
                  <div class="inner">
                    <p class="service__number">4</p>
                    <span class="service__text">Ваш документ готов</span>
                  </div>
                </div>
                <div class="back">
                  <div class="inner">
                    <p>
                      Ваш документ должны обработать, после чего можете забрать
                      готовый документ
                    </p>
                  </div>
                </div>
              </div>
            </li>
            <li
              id="fron-5"
              class="service__item"
              ontouchstart="this.classList.toggle('hover');"
            >
              <div class="container">
                <div class="front service-front-5">
                  <div class="inner">
                    <p class="service__number">5</p>
                    <span class="service__text">Сохраните ваш документ</span>
                  </div>
                </div>
                <div class="back">
                  <div class="inner">
                    <p>Сохраните заполненный вами документ</p>
                  </div>
                </div>
              </div>
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
    gsap.from(".service__title, .service__link, .service__desc", {
      scale: 0.1,
      opacity: 0,
      stagger: 0.2,
      rotation: 0,
      y: 200,
      duration: 0.6,
      scrollTrigger: {
        trigger: "advantages__left, .service__link ,.service__desc",
        toggleActions: "play none none none",
      },
    });
    gsap.from(".service__item", {
      scale: 0.1,
      opacity: 0,
      stagger: 0.2,
      rotation: 0,
      y: 200,
      duration: 0.6,
      scrollTrigger: {
        trigger: ".service__item",
        toggleActions: "play none none none",
      },
    });
  },
};
</script>

<style lang="scss" scoped>
._container {
  max-width: 1675px;
  margin: 0px auto;
  padding: 0px 20px;
}

@import "@/./style/veraibles.scss";
#fron-5 {
  order: 4;
  margin-top: 80px;
}
#fron-4 {
  order: 5;
  margin-bottom: 150px;
}
.service__front-1 {
  background-image: url("@/./assets/img/service-Landing/document-1.jpg");
}
.service__front-2 {
  background-image: url("@/./assets/img/service-Landing/document-2.jpg");
}
.service__front-3 {
  background-image: url("@/./assets/img/service-Landing/document-3.jpg");
}
.service-front-4 {
  background-image: url("@/./assets/img/service-Landing/document-4.jpg");
}
.service-front-5 {
  background-image: url("@/./assets/img/service-Landing/document-5.jpg");
}
.service__number {
  font-size: 100px;
  line-height: 78px;
  opacity: 0.87;
}
.service {
  padding-top: 200px;
}
.service__box-desc {
  max-width: 1000px;
}
.service__title {
  font-size: 64px;
  line-height: 78px;
  color: #000000;
  opacity: 0.87;
  margin-top: 10px;
  margin-bottom: 30px;
}
.service__link {
  font-size: 40px;
  line-height: 49px;
  color: $colorMain;
}
.service__desc {
  font-size: 40px;
  line-height: 49px;
  color: #000000;
  opacity: 0.87;
}
.service__wrapper {
  width: 100%;
  margin: 0 auto;
  max-width: 90rem;
}

.service__list {
  display: -webkit-box;
  display: -ms-flexbox;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  justify-content: space-around;
  -ms-flex-wrap: wrap;
  -webkit-box-pack: center;
  -ms-flex-pack: center;
  align-items: center;
  background-image: url("@/./assets/img/service-Landing/arrow-1.svg "),
    url("@/./assets/img/service-Landing/arrow-2.svg "),
    url("@/./assets/img/service-Landing/arrow-3.svg "),
    url("@/./assets/img/service-Landing/arrow-4.svg ");
  background-repeat: no-repeat, no-repeat, no-repeat, no-repeat;
  background-position: 800px 50px, 250px 470px, 1325px 300px, 570px 700px;
}

.service__item {
  width: 400px;
  height: 300px;
  margin: 1rem;
  cursor: pointer;
}

.service__item:nth-child(1) {
  margin-top: 150px;
}
.service__item:nth-child(2) {
  margin-top: 250px;
}
.service__item:nth-child(5) {
  margin-bottom: 200px;
}

.container {
  -webkit-transform-style: preserve-3d;
  transform-style: preserve-3d;
  -webkit-perspective: 1000px;
  perspective: 1000px;
}

.front,
.back {
  background-size: cover;
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.25);
  border-radius: 10px;
  background-position: center;
  -webkit-transition: -webkit-transform 0.7s cubic-bezier(0.4, 0.2, 0.2, 1);
  transition: -webkit-transform 0.7s cubic-bezier(0.4, 0.2, 0.2, 1);
  -o-transition: transform 0.7s cubic-bezier(0.4, 0.2, 0.2, 1);
  transition: transform 0.7s cubic-bezier(0.4, 0.2, 0.2, 1);
  transition: transform 0.7s cubic-bezier(0.4, 0.2, 0.2, 1),
    -webkit-transform 0.7s cubic-bezier(0.4, 0.2, 0.2, 1);
  -webkit-backface-visibility: hidden;
  backface-visibility: hidden;
  text-align: center;
  min-height: 280px;
  height: auto;
  border-radius: 10px;
  color: #fff;
  font-size: 1.5rem;
}

.back {
  background: #cedce7;
  background: -webkit-linear-gradient(45deg, #cedce7 0%, #596a72 100%);
  background: -o-linear-gradient(45deg, #cedce7 0%, #596a72 100%);
  background: linear-gradient(45deg, #cedce7 0%, #596a72 100%);
}

.front:after {
  position: absolute;
  top: 0;
  left: 0;
  z-index: 1;
  width: 100%;
  height: 100%;
  content: "";
  display: block;
  opacity: 0.6;
  background-color: black;
  -webkit-backface-visibility: hidden;
  backface-visibility: hidden;
  border-radius: 10px;
}
.container:hover .front,
.container:hover .back {
  -webkit-transition: -webkit-transform 0.7s cubic-bezier(0.4, 0.2, 0.2, 1);
  transition: -webkit-transform 0.7s cubic-bezier(0.4, 0.2, 0.2, 1);
  -o-transition: transform 0.7s cubic-bezier(0.4, 0.2, 0.2, 1);
  transition: transform 0.7s cubic-bezier(0.4, 0.2, 0.2, 1);
  transition: transform 0.7s cubic-bezier(0.4, 0.2, 0.2, 1),
    -webkit-transform 0.7s cubic-bezier(0.4, 0.2, 0.2, 1);
}

.back {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
}

.inner {
  -webkit-transform: translateY(-50%) translateZ(60px) scale(0.94);
  transform: translateY(-50%) translateZ(60px) scale(0.94);
  top: 50%;
  position: absolute;
  left: 0;
  width: 100%;
  padding: 2rem;
  -webkit-box-sizing: border-box;
  box-sizing: border-box;
  outline: 1px solid transparent;
  -webkit-perspective: inherit;
  perspective: inherit;
  z-index: 2;
}

.container .back {
  -webkit-transform: rotateY(180deg);
  transform: rotateY(180deg);
  -webkit-transform-style: preserve-3d;
  transform-style: preserve-3d;
}

.container .front {
  -webkit-transform: rotateY(0deg);
  transform: rotateY(0deg);
  -webkit-transform-style: preserve-3d;
  transform-style: preserve-3d;
}

.container:hover .back {
  -webkit-transform: rotateY(0deg);
  transform: rotateY(0deg);
  -webkit-transform-style: preserve-3d;
  transform-style: preserve-3d;
}

.container:hover .front {
  -webkit-transform: rotateY(-180deg);
  transform: rotateY(-180deg);
  -webkit-transform-style: preserve-3d;
  transform-style: preserve-3d;
}

.front .inner .service__number {
  font-size: 4rem;
  margin-bottom: 2rem;
  position: relative;
}

.front .inner .service__number:after {
  content: "";
  width: 4rem;
  height: 2px;
  position: absolute;
  background: #c6d4df;
  display: block;
  left: 0;
  right: 0;
  margin: 0 auto;
  bottom: -0.75rem;
}

.front .inner .service__text {
  color: #fff;
  font-weight: 600;
}

@media screen and (max-width: 1480px) {
  #fron-5 {
    order: 0;
    margin-top: 0px;
  }
  #fron-4 {
    order: 0;
    margin-bottom: 0px;
  }
  .service__item {
    width: calc(33.333333% - 2rem);
  }
  .service__list {
    background-image: url("@/./assets/img/service-Landing/arrow-1.svg "),
      url("@/./assets/img/service-Landing/arrow-2.svg "),
      url("@/./assets/img/service-Landing/arrow-3.svg "),
      url("@/./assets/img/service-Landing/arrow-4.svg ");
    background-repeat: no-repeat, no-repeat, no-repeat, no-repeat;
    background-position: 550px 50px, 100px 470px, 1000px 200px, 470px 700px;
  }
}

@media screen and (max-width: 1060px) {
  .service__title {
    font-size: 50px;
    line-height: 70px;
  }
  .service__item {
    width: calc(50% - 2rem);
  }
  .service__list {
    background-image: url("");
  }
  .service__item {
    margin-top: 0px;
  }
  .service__item:nth-child(1) {
    margin-top: 100px;
  }
  .service__item:nth-child(2) {
    margin-top: 150px;
  }
  .service__item:nth-child(5) {
    margin-bottom: 150px;
  }
  .service__box-desc {
    text-align: center;
  }
}

@media screen and (max-width: 700px) {
  .service__item {
    width: 100%;
    margin: 0 0 2rem 0;
  }
  .service__item:nth-child(1) {
    margin-top: 50px;
  }
  .service__item:nth-child(2) {
    margin-top: 0px;
  }
  .service__item:nth-child(5) {
    margin-bottom: 100px;
  }
  .service__desc {
    font-size: 35px;
    line-height: 40px;
  }
  .service__title {
    font-size: 45px;
    line-height: 40px;
  }
  @media screen and (max-width: 380px) {
    .service__title {
      font-size: 35px;
    }
    .service__desc {
      font-size: 25px;
    }
  }
}
</style>

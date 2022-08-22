<template>
  <div class="service">
    <div class="_container">
      <div class="service__wrapper">
        <div class="service__box-desc">
          <a class="service__link" href="#">Инструкция</a>
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
                <div
                  class="front"
                  style="background-image: url(https://unsplash.it/500/500/)"
                >
                  <div class="inner">
                    <p>1</p>
                    <span>Создайте необходимый документ</span>
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
                <div
                  class="front"
                  style="background-image: url(https://unsplash.it/500/500/)"
                >
                  <div class="inner">
                    <p>3</p>
                    <span>Заполните документ</span>
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
              class="service__item"
              ontouchstart="this.classList.toggle('hover');"
            >
              <div class="container">
                <div
                  class="front"
                  style="background-image: url(https://unsplash.it/500/500/)"
                >
                  <div class="inner">
                    <p>4</p>
                    <span>Ваш документ готов</span>
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
                <div
                  class="front"
                  style="background-image: url(https://unsplash.it/500/500/)"
                >
                  <div class="inner">
                    <p>5</p>
                    <span>Сохраните ваш документ</span>
                  </div>
                </div>
                <div class="back">
                  <div class="inner">
                    <p>Сохраните заполненный вами документ</p>
                  </div>
                </div>
              </div>
            </li>
            <li
              class="service__item"
              ontouchstart="this.classList.toggle('hover');"
            >
              <div class="container">
                <div
                  class="front"
                  style="background-image: url(https://unsplash.it/500/500/)"
                >
                  <div class="inner">
                    <p>5</p>
                    <span>Сохраните ваш документ</span>
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
export default {};
</script>

<style lang="scss" scoped>
@import "@/./style/veraibles.scss";
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
  background-color: #000;
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

.front .inner p {
  font-size: 2rem;
  margin-bottom: 2rem;
  position: relative;
}

.front .inner p:after {
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

.front .inner span {
  color: rgba(255, 255, 255, 0.7);
  font-family: "Montserrat";
  font-weight: 300;
}

@media screen and (max-width: 64rem) {
  .service__item {
    width: calc(33.333333% - 2rem);
  }
}

@media screen and (max-width: 48rem) {
  .service__item {
    width: calc(50% - 2rem);
  }
}

@media screen and (max-width: 32rem) {
  .service__item {
    width: 100%;
    margin: 0 0 2rem 0;
  }
}
</style>

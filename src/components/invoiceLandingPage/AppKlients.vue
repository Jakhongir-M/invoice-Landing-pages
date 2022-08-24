<template>
  <div class="klients">
    <div class="container">
      <p class="klients__desc">Клиенты</p>
      <h3 class="klients__title">Наши Основные клиенты</h3>
      <div class="klients__box">
        <div class="klients__track">
          <div class="slide">
            <img
              src="@/./assets/img/klients/icon-1.png"
              height="100"
              width="90"
              alt=""
            />
          </div>

          <div class="klients__slide">
            <img
              src="@/./assets/img/klients/icon-2.png"
              height="100"
              width="100"
              alt=""
            />
          </div>
          <div class="klients__slide">
            <img
              src="@/./assets/img/klients/icon-3.png"
              height="100"
              width="530"
              alt=""
            />
          </div>

          <div class="klients__slide">
            <img
              src="@/./assets/img/klients/icon-4.png"
              height="100"
              width="200"
              alt=""
            />
          </div>

          <div class="klients__slide">
            <img
              src="@/./assets/img/klients/icon-1.png"
              height="100"
              width="90"
              alt=""
            />
          </div>
          <div class="klients__slide">
            <img
              src="@/./assets/img/klients/icon-2.png"
              height="100"
              width="100"
              alt=""
            />
          </div>
          <div class="klients__slide">
            <img
              src="@/./assets/img/klients/icon-3.png"
              height="100"
              width="530"
              alt=""
            />
          </div>
          <div class="klients__slide">
            <img
              src="@/./assets/img/klients/icon-4.png"
              height="100"
              width="200"
              alt=""
            />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script></script>

<style scoped lang="scss">
@import "@/./style/veraibles.scss";

.klients__desc {
  font-size: 40px;
  line-height: 49px;
  color: $colorMain;
}
.klients__title {
  font-size: 64px;
  line-height: 78px;
  color: #000000;
  opacity: 0.87;
  margin-bottom: 100px;
}
@mixin white-gradient {
  background: linear-gradient(
    to right,
    rgba(255, 255, 255, 1) 0%,
    rgba(255, 255, 255, 0) 100%
  );
}

$animationSpeed: 40s;

// Animation
@keyframes scroll {
  0% {
    transform: translateX(0);
  }
  100% {
    transform: translateX(calc(-250px * 7));
  }
}

// Styling
.klients__slide {
  margin-right: 200px;
}
.klients__box {
  background: white;
  box-shadow: 0 10px 20px -5px rgba(0, 0, 0, 0.125);
  height: 100px;
  margin: auto;
  overflow: hidden;
  position: relative;
  max-width: 1500px;

  &::before,
  &::after {
    @include white-gradient;
    content: "";
    height: 100px;
    position: absolute;
    width: 200px;
    z-index: 2;
  }

  &::after {
    right: 0;
    top: 0;
    transform: rotateZ(180deg);
  }

  &::before {
    left: 0;
    top: 0;
  }

  .klients__track {
    animation: scroll $animationSpeed linear infinite;
    display: flex;

    width: calc(250px * 14);
  }

  .klients__box {
    height: 100px;
    width: 250px;
  }
}
@media screen and (max-width: 500px) {
  .klients__desc {
    font-size: 24px;
  }
  .klients__title {
    font-size: 35px;
    line-height: 40px;
  }
  .klients__slide {
    margin-right: 100px;
  }
  $animationSpeed: 10s;
}
</style>

<template>
  <div class="tariff">
    <input type="radio" name="testimonial" id="t-1" />
    <input type="radio" name="testimonial" id="t-2" checked />
    <input type="radio" name="testimonial" id="t-3" />

    <div class="tariff__testimonials">
      <label class="taiff__item" for="t-1">
        <h3>Бизнес 500</h3>
        <p>345 сум</p>
      </label>
      <label class="taiff__item" for="t-2">
        <h3>Старт</h3>
        <p>345 сум</p>
      </label>
      <label class="taiff__item" for="t-3">
        <h3>Бизнес 1000</h3>
        <p>276 сум</p>
      </label>
    </div>
    <div class="dots">
      <label for="t-1"></label>
      <label for="t-2"></label>
      <label for="t-3"></label>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped lang="scss">
@import "@/./style/veraibles.scss";
.tariff {
  margin-top: 200px;
  width: 100%;
}
.tariff input {
  display: none;
}
.tariff__testimonials {
  display: flex;
  align-items: center;
  justify-content: center;
  position: relative;
  min-height: 350px;
  perspective: 1000px;
  overflow: hidden;
}
.tariff__testimonials .taiff__item {
  top: 0;
  position: absolute;
  box-sizing: border-box;
  background-color: #fff;
  padding: 30px;
  width: 450px;
  text-align: center;
  transition: transform 0.4s;
  -webkit-transform-style: preserve-3d;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.3);
  user-select: none;
  cursor: pointer;
}
.tariff__testimonials .taiff__item {
  width: 500px;
  height: 550px;
  border-radius: 25px;
}

.dots {
  display: flex;
  justify-content: center;
  align-items: center;
}
.dots label {
  display: block;
  height: 5px;
  width: 5px;
  border-radius: 50%;
  cursor: pointer;
  background-color: #413b52;
  margin: 7px;
  transition: transform 0.2s, color 0.2s;
}
/* First */
#t-1:checked ~ .dots label[for="t-1"] {
  transform: scale(2);
  background-color: #413b52;
}
#t-1:checked ~ .dots label[for="t-2"] {
  transform: scale(1.5);
}
#t-1:checked ~ .tariff__testimonials label[for="t-1"] {
  z-index: 4;
  background-color: $colorMain;
  color: #fff;
}
#t-1:checked ~ .tariff__testimonials label[for="t-2"] {
  transform: translateX(300px) translateZ(-90px) rotateY(-15deg);
  z-index: 3;
}
#t-1:checked ~ .tariff__testimonials label[for="t-3"] {
  transform: translateX(600px) translateZ(-180px) rotateY(-25deg);
  z-index: 2;
}
#t-1:checked ~ .tariff__testimonials label[for="t-4"] {
  transform: translateX(900px) translateZ(-270px) rotateY(-35deg);
  z-index: 1;
}
#t-1:checked ~ .tariff__testimonials label[for="t-5"] {
  transform: translateX(1200px) translateZ(-360px) rotateY(-45deg);
}
/* Second */
#t-2:checked ~ .dots label[for="t-1"] {
  transform: scale(1.5);
}
#t-2:checked ~ .dots label[for="t-2"] {
  transform: scale(2);
  background-color: #413b52;
}
#t-2:checked ~ .dots label[for="t-3"] {
  transform: scale(1.5);
}
#t-2:checked ~ .tariff__testimonials label[for="t-1"] {
  transform: translateX(-300px) translateZ(-90px) rotateY(15deg);
}
#t-2:checked ~ .tariff__testimonials label[for="t-2"] {
  z-index: 3;
  color: #fff;
  background-color: $colorMain;
}
#t-2:checked ~ .tariff__testimonials label[for="t-3"] {
  transform: translateX(300px) translateZ(-90px) rotateY(-15deg);
  z-index: 2;
}
#t-2:checked ~ .tariff__testimonials label[for="t-4"] {
  transform: translateX(600px) translateZ(-180px) rotateY(-25deg);
  z-index: 1;
}
#t-2:checked ~ .tariff__testimonials label[for="t-5"] {
  transform: translateX(900px) translateZ(-270px) rotateY(-35deg);
}
/* Third */
#t-3:checked ~ .dots label[for="t-2"] {
  transform: scale(1.5);
}
#t-3:checked ~ .dots label[for="t-3"] {
  transform: scale(2);
  background-color: #413b52;
}
#t-3:checked ~ .dots label[for="t-4"] {
  transform: scale(1.5);
}
#t-3:checked ~ .tariff__testimonials label[for="t-1"] {
  transform: translateX(-600px) translateZ(-180px) rotateY(25deg);
}
#t-3:checked ~ .tariff__testimonials label[for="t-2"] {
  transform: translateX(-300px) translateZ(-90px) rotateY(15deg);
}
#t-3:checked ~ .tariff__testimonials label[for="t-3"] {
  background-color: $colorMain;
  color: #fff;
  z-index: 3;
}
#t-3:checked ~ .tariff__testimonials label[for="t-4"] {
  transform: translateX(300px) translateZ(-90px) rotateY(-15deg);
  z-index: 2;
}
#t-3:checked ~ .tariff__testimonials label[for="t-5"] {
  transform: translateX(600px) translateZ(-180px) rotateY(-25deg);
}
</style>

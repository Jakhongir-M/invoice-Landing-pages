<template>
  <a href="" class="btn btn2"><slot /></a>
</template>

<script>
import gsap from "gsap";
export default {};
</script>

<style scoped lang="scss">
@import "@/./style/_veraibles.scss";
#navigation {
  display: none;
}
.middle {
  position: absolute;
  transform: translate(-50%, -50%);
}
.btn {
  position: relative;
  display: block;
  color: white;
  font-family: "600-Montserrat";
  font-size: 20px;
  line-height: 24px;
  border: 1.5px solid #ffffff;
  padding: 18px 38px;
  overflow: hidden;
  transition: 1s all ease;
  z-index: 1;
  border-radius: 15px;
  color: #fff;
}
.btn:hover {
  color: $colorMain;
}
.btn::before {
  background: #fff;
  content: "";
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  z-index: -1;

  transition: all 0.6s ease;
}
.btn2::before {
  width: 100%;
  height: 0%;
}
.btn2:hover::before {
  height: 100%;
}
</style>

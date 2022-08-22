<template>
  <a href="" class="btn btn2"></a>
</template>

<script>
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
  display: inline-block;
  color: $colorMain;
  font-family: "600-Montserrat";
  font-size: 20px;
  line-height: 24px;
  border: 1.5px solid $colorMain;
  overflow: hidden;
  transition: 1s all ease;
  z-index: 1;
  border-radius: 15px;

  padding: 18px 38px;
}
.btn:hover {
  color: #fff;
}
.btn::before {
  background: $colorMain;
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

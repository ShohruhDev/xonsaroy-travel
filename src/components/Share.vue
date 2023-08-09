<template>
  <div :class="{ open: isOpen }" @click="toggleShare">
    <span class="share">
      <i class="fa-solid fa-share-nodes"></i>
    </span>
    <i class="line"></i>
    <a href=" https://t.me/xonsaroytravel"><i class="fab fa-telegram"></i></a>
    <a href="https://instagram.com/xonsaroy.travel?utm_source=qr&igshid=MzNlNGNkZWQ4Mg%3D%3D"
      ><i class="fab fa-instagram"></i
    ></a>
    <a href="tel:+998995566666">
      <i class="fa-solid fa-phone"></i>
    </a>
  </div>
</template>
<script setup>
import { ref } from 'vue'

const isOpen = ref(false)

const toggleShare = () => {
  isOpen.value = !isOpen.value
}
</script>
<style scoped>
a:hover {
  color: black;
}
* {
  box-sizing: border-box;
}
div {
  color: #fff;
  width: 40px;
  text-align: center;
  margin: auto;
  position: absolute;
  right: 50px;
}
@media (max-width: 425px) {
  div {
    bottom: 30px;
    right: 20px;
  }
}
.share,
a {
  width: 40px;
  height: 40px;
  display: inline-block;
  border-radius: 30px;
  margin: 5px auto;
  cursor: pointer;
  position: relative;
  color: white;
}
div i {
  margin-top: 10px;
  font-size: 20px;
}
.share {
  background: #3fbad8;
}
a:nth-of-type(1) {
  background-position: -115px center;
}
a:nth-of-type(2) {
  background-position: -48px center;
}
a:nth-of-type(3) {
  background-position: 17px center;
}

.line {
  height: 0;
}
a {
  -webkit-transform: scale(0) translate3d(0, 0, 0);
  -webkit-transition:
    -webkit-transform 0.0001s linear,
    background 0.0001s ease;
}

/* animation */
div.open i {
  height: 190px;
  -webkit-transition: height 0.0001s linear;
  -webkit-transition-duration: 0.3s;
}
div.open a {
  background-color: #51cf66;
  -webkit-transform: scale(1) translate3d(0, 0, 0);
  -webkit-transition-delay: 0.1s, 0.0001s;
  -webkit-transition-duration: 0.3s, 0.4s;
}
div.open a:nth-of-type(2) {
  -webkit-transition-delay: 0.2s, 0.0001s;
}
div.open a:nth-of-type(3) {
  -webkit-transition-delay: 0.3s, 0.001s;
}
</style>

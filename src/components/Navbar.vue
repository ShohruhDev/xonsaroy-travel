<template>
  <div>
    <header>
      <div class="header_content">
        <div class="logo">
          <a href="/">
            <img class="logo" src="../img/logog.svg" alt="logo" />
          </a>
        </div>
        <div class="navs">
          <nav>
            <a href="#about"
              ><span>{{ $t('navbar.aboutus') }}</span></a
            >
            <a href="#adv"
              ><span>{{ $t('navbar.turs') }}</span></a
            >
            <a href="#footer"
              ><span>{{ $t('navbar.contacts') }}</span></a
            >
            <i id="mobile-btn" class="fas fa-bars" @click="handleClick"></i>
            <LanguageSwitcher class="language" />
          </nav>
        </div>
      </div>
    </header>
    <div class="mobile_navs" :style="{ visibility: active ? 'visible' : 'hidden' }">
      <a class="close" @click="active = false">
        <i class="fa-regular fa-circle-xmark"></i>
      </a>
      <a href="#about"
        ><span>{{ $t('navbar.aboutus') }}</span></a
      >
      <a href="#adv"
        ><span>{{ $t('navbar.turs') }}</span></a
      >
      <a href="#footer"
        ><span>{{ $t('navbar.contacts') }}</span></a
      >
      <LanguageSwitcher class="switcher" />
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import LanguageSwitcher from './LanguageSwitcher.vue'

const active = ref(false)

const handleClick = () => {
  active.value = !active.value
}
</script>

<style scoped>
header {
  margin-bottom: 20px;
}
.close {
  position: absolute;
  top: 20px;
  right: 30px;
}

.logo {
  width: 175px;
  height: 175px;
}
nav i {
  display: none;
}
header {
  width: 100vw;
  height: auto;
  position: absolute;
  top: 0;
  z-index: 3;
}
nav {
  display: flex;
  align-items: center;
}
.header_content {
  height: auto;
  width: auto;
  padding: 0px 160px;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
}
nav a span:hover {
  color: #51cf66;
  transition: 0.5s ease all;
}
@media (max-width: 1199px) {
  .header_content {
    padding: 27px 70px;
  }
}

@media (max-width: 600px) {
  .header_content {
    padding: 27px 24px;
  }
}

@media (max-width: 767px) {
  nav i {
    display: block;
    color: white;
    font-size: 20px;
  }
  .navs nav a {
    display: none;
  }
  .navs nav .language {
    display: none;
  }
  .mobile_navs {
    visibility: visible;
  }
}
@media (min-width: 768px) {
  .mobile_navs {
    visibility: hidden;
  }
}
@media (min-width: 768px) {
  .navs nav a {
    display: contents;
    font-family: 'Montserrat', sans-serif;
    color: white;
    font-style: normal;
    font-weight: 500;
    font-size: 14px;
    line-height: 17px;
    text-decoration: none;
    transition: 0.5s ease all;
  }
}

.navs nav a span {
  display: inline-block;
  margin: 0px 10px;
}

.mobile_navs {
  position: absolute;
  height: 75vh;
  width: 100%;
  background: black;
  opacity: 0.8;
  z-index: 1999;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

@media screen and (max-width: 560px) {
  .logo {
    width: 150px;
    height: 150px;
  }
  .mobile_navs {
    visibility: visible;
  }
}

.mobile_navs a {
  text-align: center;
  font-style: normal;
  font-weight: 600;
  font-size: 19px;
  line-height: 23px;
  display: flex;
  align-items: center;
  color: #ffffff;
  text-decoration: none;
  opacity: 0.8;
  margin: 10px 0px;
  cursor: pointer;
}
</style>

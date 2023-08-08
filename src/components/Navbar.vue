<template>
  <header>
    <div class="header_content">
      <div class="logo">
        <a href="/">
          <!-- <img src="../img/logo_white.png" alt="logo" /> -->
          <img class="logo" src="../img/logo_xonsaroy.svg" alt="logo" />
        </a>
      </div>
      <div class="navs">
        <nav>
          <a href="#"
            ><span>{{ $t('navbar.aboutus') }}</span></a
          >
          <a href="#"
            ><span>{{ $t('navbar.turs') }}</span></a
          >
          <a href="#"
            ><span>{{ $t('navbar.contacts') }}</span></a
          >
          <i id="mobile-btn" class="fas fa-bars"></i>
          <LanguageSwitcher />
        </nav>
      </div>
    </div>
  </header>
  <div class="mobile_navs">
    <a href="#"><span>Главная</span></a>
    <a href="#"><span>Экскурсии</span></a>
    <a href="#"><span>Личный кабинет</span></a>
    <LanguageSwitcher />
  </div>
</template>
<script setup>
import LanguageSwitcher from './LanguageSwitcher.vue'
</script>
<style scoped>
.logo {
  width: 150px;
  height: 150px;
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
  height: 100vh;
  width: 100%;
  background: #384d70;
  z-index: 1999;
  margin-top: 100px;
  display: flex;
  flex-direction: column;
  visibility: hidden;
  align-items: center;
  justify-content: center;
}

@media screen and (max-width: 560px) {
  .logo {
    width: 120px;
    height: 120px;
  }
  .mobile_navs {
    margin-top: 100px;
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

.mobile_navs a:hover {
  color: #b6b6b6fa;
}

.mobile_navs .btn_wrapper {
  padding-top: 50px;
}

.mobile_navs .header_btn_mob {
  padding: 11px 30px;
  border-radius: 10px;
  border: none;
  font-style: normal;
  font-weight: 600;
  font-size: 15px;
  line-height: 18px;
  color: white;
}
</style>

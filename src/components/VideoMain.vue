<template>
  <section class="videolazy">
    <div class="video_content">
      <img
        src="https://images.unsplash.com/photo-1433838552652-f9a46b332c40?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2370&q=80"
        alt=""
      />
      <div class="info_video_content">
        <div v-if="locale === 'ru'" class="slogo">
          <span class="travel">ПУТЕШЕСТВУЙ</span>
          <span class="without">вместе с</span>
          <span class="company_name">Xon Saroy TRAVEL</span>
          <a href="#tours" class="btn_lazy">К турам <i class="fas fa-long-arrow-alt-right"></i></a>
        </div>
        <div v-else-if="locale === 'uz'" class="slogo">
          <span class="company_name">Xon Saroy TRAVEL</span>
          <span class="without">bilan birga</span>
          <span class="travel">SAYOHAT QILING</span>
          <a href="#tours" class="btn_lazy"
            >{{ $t('video.totours') }} <i class="fas fa-long-arrow-alt-right"></i
          ></a>
        </div>
        <Share />
      </div>
    </div>
  </section>
</template>

<script setup>
import Share from './Share.vue'
import { useI18n } from 'vue-i18n'
const { locale } = useI18n({ useScope: 'global' })
</script>

<style scoped>
.company_name {
  text-transform: uppercase;
}
.videolazy {
  width: 100vw;
  height: 80vh;
  position: relative;
}

.video_content {
  width: 100%;
  height: 100%;
  position: relative;
}

.video_content img {
  object-fit: cover;
  position: absolute;
  z-index: 1;
  top: 0;
  left: 0;
  height: 80vh;
  width: 100%;
}
@media (max-width: 1024px) {
  .video_content {
    height: 75vh;
  }
  .video_content video {
    height: 75vh;
    object-fit: none;
    width: 100vw;
  }
}
@media (max-width: 768px) {
  .info_video_content {
    height: 60%;
  }
}
.info_video_content {
  position: absolute;
  /* width: calc(100vw - 320px); */
  width: 100%;
  height: 100%;
  z-index: 2;
  top: 0;
  left: 0;
  background-color: rgba(0, 0, 0, 0.2);
  padding: 0px 160px;
  display: flex;
  align-items: center;
}

@media (max-width: 1199px) {
  .info_video_content {
    padding: 0px 70px;
    height: 75vh;
  }
}

@media (max-width: 600px) {
  .info_video_content {
    padding: 0px 24px;
  }
}

.slogo {
  position: relative;
}
.slogo .travel {
  font-family: 'Montserrat';
  font-style: normal;
  font-weight: 700;
  font-size: 72px;
  line-height: 88px;
  color: #ffffff;
  display: block;
}

@media (max-width: 886px) {
  .slogo .travel {
    font-size: 48px;
  }
}

@media (max-width: 624px) {
  .slogo .travel {
    font-size: 36px;
  }
}

@media (max-width: 380px) {
  .slogo .travel {
    font-size: 28px;
  }
}

.slogo .without {
  position: absolute;
  font-family: 'Lobster';
  font-style: normal;
  font-weight: 400;
  font-size: 50px;
  line-height: 64px;
  color: #ffc700;
  left: 500px;
  display: block;
  top: 55px;
}

@media (max-width: 886px) {
  .slogo .without {
    left: 250px;
    font-size: 40px;
  }
}

@media (max-width: 624px) {
  .slogo .without {
    left: 150px;
    font-size: 40px;
  }
}

@media (max-width: 380px) {
  .slogo .without {
    left: 150px;
    font-size: 25px;
  }
}

.company_name {
  font-family: 'Bricolage Grotesque';
  font-style: normal;
  font-weight: 600;
  font-size: 96px;
  line-height: 117px;
  color: white;
  -webkit-text-stroke-width: 1px;
  -webkit-text-stroke-color: #ffffff;
  padding: 0;
  margin: 0;
}

@media (max-width: 885px) {
  .company_name {
    display: block;
    line-height: 96px;
    padding-top: 10px;
  }
}

@media (max-width: 624px) {
  .company_name {
    font-size: 72px;
    line-height: 72px;
  }
}

@media (max-width: 380px) {
  .company_name {
    font-size: 50px;
    line-height: 50px;
  }
}

.btn_lazy {
  width: 230px;
  height: 50px;
  background: linear-gradient(92.71deg, #0499dd 0%, #17c1bc 100%);
  border-radius: 60px;
  margin-top: 60px;
  font-family: 'Montserrat';
  font-style: normal;
  font-weight: 700;
  font-size: 14px;
  line-height: 17px;
  color: #ffffff;
  text-decoration: none;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
  transition: 0.5s ease all;
}

.btn_lazy i {
  margin-left: 5px;
}

.btn_lazy:hover {
  transition: 0.5s ease all;
  background: linear-gradient(92.71deg, #0287c5 0%, #13928e 100%);
}
</style>

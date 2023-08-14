<template>
  <section class="popular" id="tours">
    <div class="popular_content">
      <div class="title_content">
        <div class="title">
          <span>{{ $t('tours.title') }}</span>
        </div>
      </div>
      <div class="popular_slider">
        <swiper
          :slidesPerView="'auto'"
          :spaceBetween="30"
          :pagination="{
            clickable: true
          }"
          :modules="modules"
        >
          <swiper-slide
            v-for="(item, index) in popularItems"
            :key="index"
            class="popular_item"
            :style="{
              backgroundImage: `url(${item.imgSrc})`,
              backgroundSize: 'cover'
            }"
          >
            <div class="title">
              <span>{{ item.title }}</span>
            </div>
            <div class="pricetime">
              <div class="time">
                <i class="fas fa-clock"></i>
                <span>{{ item.duration }}</span>
              </div>
              <div class="price">
                <i class="fas fa-coins"></i>
                <span>{{ item.price }}</span>
              </div>
            </div>
            <div class="about">
              <p>{{ item.description }}</p>
            </div>
          </swiper-slide>
        </swiper>
      </div>
    </div>
  </section>
</template>

<script setup>
import { Swiper, SwiperSlide } from 'swiper/vue'
import 'swiper/css'
import 'swiper/css/navigation'
import { Navigation } from 'swiper/modules'
import { useI18n } from 'vue-i18n'

const modules = [Navigation]
import { reactive, watch } from 'vue'

const { t, locale } = useI18n({ useScope: 'global' })

const popularItems = reactive([
  {
    title: t('tours.umra.title'),
    duration: `7 ${t('tours.days')}`,
    price: '1500 $',
    description: t('tours.umra.description'),
    imgSrc:
      'https://images.unsplash.com/photo-1580418827493-f2b22c0a76cb?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1287&q=80'
  },
  {
    title: t('tours.antalya.title'),
    duration: `7 ${t('tours.days')}`,
    price: '780 $',
    description: t('tours.antalya.description'),
    imgSrc:
      'https://images.unsplash.com/photo-1578852952104-54f3dac8b260?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=927&q=80'
  },
  {
    title: t('tours.dubai.title'),
    duration: `7 ${t('tours.days')}`,
    price: '420 $',
    description: t('tours.dubai.description'),
    imgSrc:
      'https://images.unsplash.com/photo-1518684079-3c830dcef090?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1287&q=80'
  },
  {
    title: t('tours.istambul.title'),
    duration: `7 ${t('tours.days')}`,
    price: '738 $',
    description: t('tours.istambul.description'),
    imgSrc:
      'https://images.unsplash.com/photo-1633505191034-2763b7aa980c?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1288&q=80'
  },
  {
    title: t('tours.sharmlsheyx.title'),
    duration: `7 ${t('tours.days')}`,
    price: '590 $',
    description: t('tours.sharmlsheyx.description'),
    imgSrc:
      'https://images.unsplash.com/photo-1568322445389-f64ac2515020?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1277&q=80'
  },
  {
    title: t('tours.batumi.title'),
    duration: `7 ${t('tours.days')}`,
    price: '650 $',
    description: t('tours.batumi.description'),
    imgSrc:
      'https://images.unsplash.com/photo-1622383693127-a8d29be7ab7d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1335&q=80'
  },
  {
    title: t('tours.shrilanka.title'),
    duration: `7 ${t('tours.days')}`,
    price: '1100 $',
    description: t('tours.shrilanka.description'),
    imgSrc:
      'https://images.unsplash.com/photo-1638434367723-ccfb703e0314?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1335&q=80'
  }
])
watch(
  () => locale.value,
  (newLocale) => {
    popularItems.forEach((item, index) => {
      item.title = t(`tours.${item.localeKey}.title`)
      item.description = t(`tours.${item.localeKey}.description`)
    })
  }
)
</script>

<style scoped>
.popular {
  width: 100vw;
  height: auto;
}

.popular_content {
  height: 80vh;
  padding: 0px 160px;
  margin-bottom: 100px;
}

@media (max-width: 768px) {
  .popular_content {
    padding: 0px 79px;
  }
}

.title_content {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  margin-bottom: 50px;
  margin-top: 100px;
}

.title_content .title {
  font-family: 'Montserrat', sans-serif;
  font-style: normal;
  font-weight: 700;
  font-size: 24px;
  line-height: 29px;
  color: #0499dd;
}

.popular_slider {
  position: absolute;
  width: 100%;
  z-index: 1;
  right: 0;
}

.popular_item {
  cursor: pointer;
  width: 400px;
  height: 497px;
  border-radius: 10px;
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
  padding: 16px;
  display: flex;
  flex-direction: column;
  justify-content: end;
  margin: 0px 20px;
}

@media (max-width: 768px) {
  .popular_item {
    width: 300px;
  }
}

.popular_item .title span {
  font-family: 'Montserrat';
  font-style: normal;
  font-weight: 700;
  font-size: 14px;
  line-height: 17px;
  color: #ffc700;
}

.popular_item .pricetime {
  display: flex;
  flex-direction: row;
  margin: 10px;
}

.pricetime .time {
  font-family: 'Montserrat';
  font-style: normal;
  font-weight: 500;
  font-size: 12px;
  line-height: 15px;
  color: #ffffff;
}

.pricetime .time span {
  margin-left: 5px;
}

.pricetime .price {
  font-family: 'Montserrat';
  font-style: normal;
  font-weight: 500;
  font-size: 12px;
  line-height: 15px;
  color: #ffffff;
  margin-left: 10px;
}

.pricetime .price span {
  margin-left: 5px;
}

.about {
  font-family: 'Montserrat';
  font-style: normal;
  font-weight: 500;
  font-size: 12px;
  line-height: 15px;
  color: #ffffff;
  margin-bottom: 10px;
}
</style>

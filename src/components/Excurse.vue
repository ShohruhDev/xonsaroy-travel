<template>
  <section class="excurse">
    <div class="excurse_content">
      <div class="title">
        <span>{{ $t('advantages.title') }}</span>
      </div>
      <div class="main_content">
        <div class="content_item" v-for="excursion in excursions" :key="excursion.id">
          <div class="item">
            <div class="img">
              <i class="img-logo" :class="excursion.imgClass"></i>
            </div>
            <div class="text">
              <div class="text_title">
                <span>{{ excursion.title }}</span>
              </div>
              <div class="main_text">
                <p>{{ excursion.description }}</p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { useI18n } from 'vue-i18n'
const { t } = useI18n({ useScope: 'global' })
const excursions = [
  {
    id: 1,
    imgClass: 'fas fa-people-arrows',
    imgAlt: 'bus',
    title: t('advantages.whywe.title'),
    description: t('advantages.whywe.description')
  },
  {
    id: 2,
    imgClass: 'far fa-comments',
    imgAlt: 'ship',
    title: t('advantages.help.title'),
    description: t('advantages.help.description')
  },
  {
    id: 3,
    imgClass: 'far fa-map',
    imgAlt: 'car',
    title: t('advantages.organization.title'),
    description: t('advantages.organization.description')
  },
  {
    id: 4,
    imgClass: 'fa-regular fa-square-check',
    imgAlt: 'canion',
    title: t('advantages.quality.title'),
    description: t('advantages.quality.description')
  }
]
</script>

<style scoped>
.excurse {
  height: auto;
  width: auto;
  padding: 0px 160px;
  margin-bottom: 100px;
}

@media (max-width: 768px) {
  .excurse {
    padding: 0px 79px;
  }
}

@media (max-width: 428px) {
  .excurse {
    padding: 0px 24px;
  }
}

.excurse .excurse_content {
  width: 100%;
  height: auto;
}

.excurse .excurse_content .title {
  font-family: 'Montserrat';
  font-style: normal;
  font-weight: 700;
  font-size: 24px;
  line-height: 29px;
  color: #0499dd;
}

.excurse .excurse_content .main_content {
  display: grid;

  grid-template-rows: 1fr 1fr;
  grid-template-columns: 1fr 1fr;
  margin-top: 90px;
}

@media (max-width: 1280px) {
  .excurse .excurse_content .main_content {
    display: flex;
    flex-direction: column;
  }
}

.excurse .excurse_content .main_content .content_item {
  display: flex;
  flex-direction: column;
}

.excurse .excurse_content .main_content .content_item .item {
  width: 90%;
  display: flex;
  flex-direction: row;
}

.excurse .excurse_content .main_content .content_item .item .img {
  margin-right: 20px;
  font-size: 40px;
  color: #13928e;
}

.excurse .excurse_content .main_content .content_item .item .text {
  display: flex;
  flex-direction: column;
}

.excurse .excurse_content .main_content .content_item .item .text .text_title {
  font-family: 'Montserrat';
  font-style: normal;
  font-weight: 700;
  font-size: 18px;
  line-height: 22px;
  color: #0499dd;
}

.excurse .excurse_content .main_content .content_item .item .text .main_text {
  font-family: 'Montserrat';
  font-style: normal;
  font-weight: 500;
  font-size: 14px;
  line-height: 17px;
  color: #282828;
}
</style>

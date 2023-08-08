<template>
  <div class="language-switcher">
    <select @input="switchLang" id="language" v-model="selectedLanguage" class="select">
      <option value="uz">Uz</option>
      <option value="ru">Ru</option>
    </select>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import { useI18n } from 'vue-i18n'
const { locale } = useI18n({ useScope: 'global' })
const selectedLanguage = ref('uz')
const switchLang = () => {
  locale.value === 'ru' ? (locale.value = 'uz') : (locale.value = 'ru')
  localStorage.setItem('lang', locale.value)
}
</script>

<style scoped>
.language-switcher {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 20px;
}

.select {
  padding: 5px;
  font-size: 16px;
}

.flag-container {
  margin-top: 10px;
}
</style>

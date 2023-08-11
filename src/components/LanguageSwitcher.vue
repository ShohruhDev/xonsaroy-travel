<template>
  <div class="language-switcher">
    <div class="selected-language" @click="toggleDropdown">
      <img :src="selectedLanguage.flag" :alt="selectedLanguage.name" class="flag-icon" />
      <span class="language-name">{{ selectedLanguage.name }}</span>
    </div>
    <div v-if="isDropdownOpen" class="language-options">
      <div
        v-for="(language, index) in languages"
        :key="index"
        class="language-option"
        @click="changeLanguage(language)"
      >
        <img :src="language.flag" :alt="language.name" class="flag-icon" />
        <span class="language-name">{{ language.name }}</span>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'
import { useI18n } from 'vue-i18n'
const { locale } = useI18n({ useScope: 'global' })

const isDropdownOpen = ref(false)
const selectedLanguage = ref({
  name: 'Russian',
  flag: 'https://upload.wikimedia.org/wikipedia/en/thumb/f/f3/Flag_of_Russia.svg/510px-Flag_of_Russia.svg.png',
  locale: 'ru'
})

const languages = [
  {
    name: 'Uzbek',
    flag: 'https://upload.wikimedia.org/wikipedia/commons/thumb/8/84/Flag_of_Uzbekistan.svg/510px-Flag_of_Uzbekistan.svg.png',
    locale: 'uz'
  },
  {
    name: 'Russian',
    flag: 'https://upload.wikimedia.org/wikipedia/en/thumb/f/f3/Flag_of_Russia.svg/510px-Flag_of_Russia.svg.png',
    locale: 'ru'
  }
]

const toggleDropdown = () => {
  isDropdownOpen.value = !isDropdownOpen.value
}

const changeLanguage = (language) => {
  selectedLanguage.value = language
  isDropdownOpen.value = false
  locale.value = language.locale
}
</script>

<style scoped>
.language-switcher {
  position: relative;
  display: inline-block;
}

.selected-language {
  cursor: pointer;
  display: flex;
  align-items: center;
  padding: 8px;
  /* border: 1px solid #ccc; */
  border-radius: 4px;
  color: #fff;
}

.flag-icon {
  width: 24px;
  height: 16px;
  margin-right: 8px;
}

.language-options {
  position: absolute;
  top: 100%;
  left: 0;
  background-color: #fff;
  border: 1px solid #ccc;
  border-top: none;
  border-radius: 4px;
  width: 100%;
}

.language-option {
  display: flex;
  align-items: center;
  padding: 8px;
  cursor: pointer;
}

.language-option:hover {
  background-color: #f0f0f0;
}
.language-name {
  margin-right: 5px;
}
</style>

<template>
  <div>
    <div v-if="loading">
      <main>
        <span class="loader"></span>
        <!-- <h1 class="loader__text">Welcome to Xonsaroy Tour Agency !!!</h1> -->
      </main>
    </div>
    <div v-else>
      <Navbar />
      <VideoMain />
      <About />
      <Popular></Popular>
      <Excurse></Excurse>
      <Gallery />
      <YandexMap />
      <Footer></Footer>
    </div>
  </div>
</template>

<script setup>
import { ref, onMounted } from 'vue'
const loading = ref(true)

import VideoMain from './components/VideoMain.vue'
import About from './components/About.vue'
import Excurse from './components/Excurse.vue'
import Gallery from './components/Gallery.vue'
import Footer from './components/Footer.vue'
import Popular from './components/Popular.vue'
import YandexMap from './components/YandexMap.vue'
import Navbar from './components/Navbar.vue'

onMounted(() => {
  setTimeout(() => {
    loading.value = false
  }, 3000)
})
</script>

<style scoped>
main {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  width: 100vw;
  height: 100vh;
  color: #24262d;
}
/* .loader__text {
  color: #0499dd;
  width: 50%;
  text-align: center;
} */
.loader {
  --loader-size: 50px;
  --loader-border-size: 4px;
  --loader-border-color: #0499dd;
  width: var(--loader-size);
  height: var(--loader-size);
  border: var(--loader-border-size) solid var(--loader-border-color);
  border-top-color: transparent;
  border-right-color: transparent;
  border-bottom-color: transparent;
  background-color: transparent;
  border-radius: 50%;
  position: relative;
  animation: rotateX 1s infinite linear;
}

.loader::before {
  content: '';
  border: var(--loader-border-size) solid var(--loader-border-color);
  border-top-color: transparent;
  border-left-color: transparent;
  border-bottom-color: transparent;
  background-color: transparent;
  border-radius: 50%;
  position: absolute;
  top: 2px;
  left: 2px;
  right: 2px;
  bottom: 2px;
  animation: rotateX 0.5s infinite linear reverse;
}

@keyframes rotateX {
  from {
    transform: rotateZ(0deg);
  }
  to {
    transform: rotateZ(360deg);
  }
}
</style>

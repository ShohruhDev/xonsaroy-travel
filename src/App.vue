<template>
  <div>
    <Navbar />
    <VideoMain />
    <About />
    <Popular></Popular>
    <Excurse></Excurse>
    <Gallery />
    <Contact />
    <YandexMap />
    <Footer></Footer>
  </div>
</template>
<script setup>
import VideoMain from './components/VideoMain.vue'
import About from './components/About.vue'
import Excurse from './components/Excurse.vue'
import Gallery from './components/Gallery.vue'
import Contact from './components/Contact.vue'
import Footer from './components/Footer.vue'
import Popular from './components/Popular.vue'
import YandexMap from './components/YandexMap.vue'
import Navbar from './components/Navbar.vue'
</script>
<style></style>

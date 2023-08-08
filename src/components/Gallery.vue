<template>
  <section class="gallery">
    <div class="gallery_title">
      <div class="title">
        <span>{{ $t('galery') }}</span>
      </div>
    </div>
    <div class="gallery_content">
      <div
        v-for="image in images"
        :key="image.id"
        :class="'gallery_item gallery_item--' + image.id"
      >
        <img :src="image.src" class="gallery_img" />
      </div>
    </div>
  </section>
</template>

<script setup>
const images = [
  {
    id: 1,
    src: 'https://images.pexels.com/photos/1266831/pexels-photo-1266831.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2'
  },
  { id: 2, src: 'https://i.ibb.co/KKYn9LV/pexels-david-bartus-586687.jpg' },
  {
    id: 3,
    src: 'https://i.ibb.co/sjc6N8C/pexels-esteban-santiago-gonzalez-12314825.jpg'
  },
  {
    id: 4,
    src: 'https://i.ibb.co/r5B7xR6/pexels-janiere-fernandez-2405101.jpg'
  },
  { id: 5, src: 'https://i.ibb.co/fv1r9XP/pexels-eyup-beyhan-7602068.jpg' },
  {
    id: 6,
    src: 'https://images.pexels.com/photos/1271619/pexels-photo-1271619.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2'
  },
  {
    id: 7,
    src: 'https://images.pexels.com/photos/2082103/pexels-photo-2082103.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2'
  },
  {
    id: 8,
    src: 'https://images.pexels.com/photos/5227440/pexels-photo-5227440.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=2'
  }
]
</script>

<style scoped>
.gallery {
  width: auto;
  height: auto;
  padding: 50px 20px;
  background-color: white;
}

.gallery .gallery_title {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  margin-bottom: 50px;
  margin-top: 100px;
  padding: 0px 160px;
  background-color: white;
}

@media (max-width: 876px) {
  .gallery .gallery_title {
    padding: 0px 79px;
  }
}

@media (max-width: 428px) {
  .gallery .gallery_title {
    padding: 0px 24px;
  }
}

.gallery .gallery_title .title {
  font-family: 'Montserrat', sans-serif;
  font-style: normal;
  font-weight: 700;
  font-size: 24px;
  line-height: 29px;
  color: #0499dd;
}

.gallery .gallery_content {
  display: grid;
  grid-template-columns: repeat(5, 1fr);
  /* grid-template-rows: repeat(4, 10vw); */
  grid-template-rows: repeat(4, 1fr);
  grid-column-gap: 20px;
  grid-row-gap: 20px;
}

@media (max-width: 876px) {
  .gallery .gallery_content {
    grid-template-columns: repeat(3, 1fr);
  }
}

.gallery_item {
  padding: 0;
  margin: 0;
  background: linear-gradient(0deg, rgba(0, 0, 0, 0.2), rgba(0, 0, 0, 0.2)), url(.jpg);
  border-radius: 5px;
  cursor: pointer;
  position: relative;
  width: auto;
  height: auto;
}

.gallery_item img {
  transition: 0.5s all ease;
}

.gallery_item:hover img {
  transform: scale(1.05);
  transition: 0.5s all ease;
}

.gallery_img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  border-radius: 5px;
}

.gallery_item--1 {
  grid-row-start: 1;
  grid-row-end: 3;
  grid-column-start: 1;
  grid-column-end: 3;
}

@media (max-width: 876px) {
  .gallery_item--1 {
    display: none;
  }
}

.gallery_item--2 {
  grid-row-start: 1;
  grid-row-end: 5;
  grid-column-start: 3;
  grid-column-end: 3;
}

@media (max-width: 876px) {
  .gallery_item--2 {
    grid-column-start: 1;
    grid-column-end: 1;
  }
}

.gallery_item--3 {
  grid-row-start: 1;
  grid-row-end: 3;
  grid-column-start: 4;
  grid-column-end: 5;
}

@media (max-width: 876px) {
  .gallery_item--3 {
    grid-column-start: 2;
    grid-column-end: 3;
  }
}

.gallery_item--4 {
  grid-row-start: 1;
  grid-row-end: 3;
  grid-column-start: 5;
  grid-column-end: 6;
}

@media (max-width: 876px) {
  .gallery_item--4 {
    grid-column-start: 3;
    grid-column-end: 4;
  }
}

.gallery_item--5 {
  grid-row-start: 3;
  grid-row-end: 5;
  grid-column-start: 1;
  grid-column-end: 2;
}

@media (max-width: 876px) {
  .gallery_item--5 {
    display: none;
  }
}

.gallery_item--6 {
  grid-row-start: 3;
  grid-row-end: 4;
  grid-column-start: 2;
  grid-column-end: 3;
}

@media (max-width: 876px) {
  .gallery_item--6 {
    display: none;
  }
}

.gallery_item--7 {
  grid-row-start: 4;
  grid-row-end: 5;
  grid-column-start: 2;
  grid-column-end: 3;
}

@media (max-width: 876px) {
  .gallery_item--7 {
    display: none;
  }
}

.gallery_item--8 {
  grid-row-start: 3;
  grid-row-end: 5;
  grid-column-start: 4;
  grid-column-end: 6;
}

@media (max-width: 876px) {
  .gallery_item--8 {
    grid-column-start: 2;
    grid-column-end: 4;
  }
}
</style>

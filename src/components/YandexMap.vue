<template>
  <section class="map">
    <div class="map_content">
      <div class="title_map">
        <div class="title">
          <span>{{ $t('location') }}</span>
        </div>
        <div class="more">
          <a href="#" class="more">Посмотреть на карте Google</a>
        </div>
      </div>

      <div class="map_location">
        <iframe
          src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d7254.196094699305!2d67.81058055252014!3d40.141977541084515!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x38b2970018c37813%3A0x6b48c74c6c34d6f4!2sXONSAROY%20HOTEL!5e0!3m2!1sen!2s!4v1691049424717!5m2!1sen!2s"
          width="100%"
          height="450"
          style="border: 0"
          allowfullscreen="true"
          loading="lazy"
          referrerpolicy="no-referrer-when-downgrade"
        ></iframe>
      </div>
    </div>
  </section>
</template>

<style scoped>
.map {
  width: auto;
  height: auto;
  background-color: white;
  margin-bottom: 150px;
}

.map_content {
  width: auto;
  height: auto;
  display: flex;
  flex-direction: column;
}
.title_map {
  padding: 0px 160px;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  margin: 100px 0px;
}
@media (max-width: 876px) {
  .title_map {
    padding: 0px 79px;
  }
}

@media (max-width: 428px) {
  .title_map {
    padding: 0px 24px;
  }
}
.title {
  font-family: 'Montserrat', sans-serif;
  font-style: normal;
  font-weight: 700;
  font-size: 24px;
  line-height: 29px;
  color: #0499dd;
}

.more a {
  font-family: 'Montserrat';
  font-style: normal;
  font-weight: 500;
  font-size: 12px;
  line-height: 15px;
  text-decoration-line: underline;
  color: #282828;
}

@media (max-width: 442px) {
  .more a {
    display: none;
  }
}
.map_location {
  margin: 0 20px;
}
</style>

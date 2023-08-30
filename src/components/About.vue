<template>
  <section class="aboutus" id="about">
    <div class="about_content">
      <div class="about_img"></div>
      <div class="about_content_info">
        <div class="title">
          <span>{{ $t('aboutus.title') }}</span>
        </div>
        <div class="text">
          <p>
            {{ $t('aboutus.description') }}
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.aboutus {
  position: relative;
  width: 100%;
  height: 100vh;
}
.aboutus .about_img {
  position: absolute;
  left: 0;
  top: 50%;
  transform: translateY(-50%);
  background-image: url('https://images.unsplash.com/photo-1623621534850-d325a1980c7e?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2671&q=80');
  background-position: center;
  background-attachment: fixed;
  background-size: cover;
  width: 70%;
  height: 80vh;
  border-radius: 0px 10px 10px 0px;
}

.aboutus .about_content_info {
  padding: 60px 85px;
  position: absolute;
  width: auto;
  height: auto;
  background: #ededed;
  border-radius: 10px;
  z-index: 2;
  top: 50%;
  transform: translateY(-50%);
  right: 20%;
}
@media (max-width: 850px) {
  .aboutus .about_content_info {
    margin: 0 24px;
    right: 0px;
    padding: 20px 25px;
    width: 50%;
  }
}

.aboutus .about_content_info .title span {
  font-family: 'Montserrat';
  font-style: normal;
  font-weight: 700;
  font-size: 24px;
  line-height: 29px;
  color: #0499dd;
}

.aboutus .about_content_info .text {
  max-width: 380px;
}

.aboutus .about_content_info .text p {
  font-family: 'Montserrat';
  font-style: normal;
  font-weight: 500;
  font-size: 14px;
  line-height: 24px;
  color: #282828;
}
@media (max-width: 650px) {
  /* .aboutus .about_content_info .text p {
    display: -webkit-box;
    -webkit-line-clamp: 20;
    -webkit-box-orient: vertical;
    overflow: hidden;
    text-overflow: ellipsis;
  } */
  .aboutus .about_img {
    width: 100%;
    border-radius: 10px;
  }
  .aboutus .about_content_info {
    width: 100%;
    margin: 0;
    top: 100%;
  }
  .aboutus .about_content_info .text {
    max-width: 100%;
  }
  .popular {
    margin-top: 300px;
  }
}
</style>

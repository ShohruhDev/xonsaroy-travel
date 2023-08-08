<template>
  <footer>
    <div class="footer_content">
      <div class="img">
        <a href="/">
          <img class="logo" src="../img/logo_xonsaroy.svg" alt="logo" />
        </a>
      </div>
      <div class="navs">
        <a href="#">{{ $t('navbar.aboutus') }}</a>
        <a href="#">{{ $t('navbar.turs') }}</a>
        <a href="#">{{ $t('navbar.contactwithus') }}</a>
      </div>
      <div class="contact_footer">
        <a href="tel:+998995566666">
          <i class="fab fa-whatsapp"></i>
          +998 995566666
        </a>
        <a href=" https://t.me/xonsaroytravel">
          <i class="fab fa-telegram"></i>
          https://t.me/xonsaroytravel
        </a>
        <a href="#">
          <i class="fab fa-telegram"></i>
          +998 995566666
        </a>
      </div>
      <div class="social_footer">
        <div class="mail">
          <i class="fas fa-envelope"></i>
          <span> xonsaroytravel@gmail.com </span>
        </div>
        <div class="social">
          <a href="https://instagram.com/xonsaroy.travel?utm_source=qr&igshid=MzNlNGNkZWQ4Mg%3D%3D"
            ><i id="ins" class="fab fa-instagram"></i
          ></a>
        </div>
      </div>
    </div>
  </footer>
</template>

<script setup></script>

<style>
.logo {
  width: 150px;
  height: 150px;
}
@media screen and (max-width: 560px) {
  .logo {
    width: 120px;
    height: 120px;
  }
}
footer {
  background: #ededed;
  width: auto;
  height: auto;
}

footer .footer_content {
  padding: 45px 77px;
  display: flex;
  flex-direction: row;
  justify-content: space-around;
  align-items: center;
}

@media (max-width: 624px) {
  footer .footer_content {
    padding: 45px 40px;
  }
}

@media (max-width: 380px) {
  footer .footer_content {
    padding: 45px 10px;
  }
}

@media (max-width: 886px) {
  footer .footer_content {
    flex-direction: column;
    justify-content: center;
  }
}

footer .footer_content .navs a {
  display: flex;
  flex-direction: column;
  font-family: 'Montserrat';
  font-style: normal;
  font-weight: 500;
  font-size: 14px;
  line-height: 15px;
  color: #282828;
  margin: 8px 0px;
  text-decoration: none;
  transition: 0.5s ease all;
}

footer .footer_content .navs a:hover {
  color: #51cf66;
  transition: 0.5s ease all;
}

@media (max-width: 886px) {
  footer .footer_content .navs {
    border-bottom: 1px solid black;
    width: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 10px 0px;
  }
}
.contact_footer {
  display: flex;
  flex-direction: column;
}
.contact_footer a {
  font-family: 'Montserrat';
  font-style: normal;
  font-weight: 500;
  font-size: 14px;
  line-height: 15px;
  color: #282828;
  text-decoration: none;
  margin: 8px 0px;
  transition: 0.5s ease all;
}

.contact_footer a:hover {
  color: #51cf66;
  transition: 0.5s ease all;
}

@media (max-width: 886px) {
  .contact_footer {
    border-bottom: 1px solid black;
    width: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 10px 0px;
  }
}

.social_footer {
  display: flex;
  flex-direction: column;
}

@media (max-width: 886px) {
  .social_footer {
    width: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 10px 0px;
  }
}

.mail span {
  font-family: 'Montserrat';
  font-style: normal;
  font-weight: 500;
  font-size: 14px;
  line-height: 17px;
  color: #282828;
  transition: 0.5s ease all;
  cursor: pointer;
}

.mail span:hover {
  color: #51cf66;
  transition: 0.5s ease all;
}

.social {
  display: flex;
  flex-direction: row;
  text-align: center;
  margin-top: 17px;
}

.social i {
  margin-right: 10px;
}

.social #vk {
  font-size: 20px;
  color: #bc0000;
}

.social #ins {
  font-size: 20px;
  color: #e59b06;
}

.social #fb {
  font-size: 20px;
  color: #17c1bc;
}
</style>

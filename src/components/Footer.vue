<template>
  <footer id="footer">
    <div class="footer_content">
      <div class="img">
        <a href="/">
          <img class="logo" src="../img/logo_xonsaroy.svg" alt="logo" />
        </a>
      </div>
      <div class="navs">
        <a href="#about">{{ $t('navbar.aboutus') }}</a>
        <a href="#adv">{{ $t('navbar.turs') }}</a>
        <a href="tel:+998995566666">{{ $t('navbar.contactwithus') }}</a>
      </div>
      <div class="contact_footer">
        <a href=" https://t.me/xonsaroytravel">
          <i class="fab fa-telegram"></i>
          https://t.me/xonsaroytravel
        </a>
        <a href="tel:+998995566666">
          <i class="fa-solid fa-phone"></i>
          +998 93 301 05 75
        </a>
      </div>
      <div class="social_footer">
        <a href="mailto:xonsaroytravel@gmail.com" class="mail">
          <i class="fas fa-envelope"></i>
          xonsaroytravel@gmail.com
        </a>
        <div class="social">
          <a href="https://instagram.com/xonsaroy.travel?utm_source=qr&igshid=MzNlNGNkZWQ4Mg%3D%3D"
            ><i id="ins" class="fab fa-instagram"></i>
            instagram.com/xonsaroy.travel
          </a>
        </div>
        <div>
          <a
            class="social_payme"
            href="https://payme.uz/fallback/merchant/?id=64d4bb6b8aff6373c2ddd4d1"
          >
            <img
              src="https://cdn.paycom.uz/documentation_assets/payme_01.svg?target=_blank"
              alt=""
            />
          </a>
        </div>
      </div>
    </div>
  </footer>
</template>

<script setup></script>

<style scoped>
a {
  color: inherit;
  text-decoration: none;
}
a:hover {
  text-decoration: none;
  color: #51cf66;
  transition: 0.5s ease all;
}
.logo {
  width: 150px;
  height: 150px;
}
.social_payme {
  width: 10px;
  height: 10px;
  padding-top: 10px;
}
.social_payme img {
  width: 100px;
  height: 60px;
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

.social {
  display: flex;
  flex-direction: row;
  text-align: center;
  margin-top: 17px;
}

.social #ins {
  font-size: 20px;
  color: #e59b06;
}
</style>

<template>
  <section class="contact">
    <div class="contact_content">
      <div class="contact_form">
        <div class="title">
          <span class="main">{{ $t('contactus.title') }}</span>
          <span class="other"> {{ $t('contactus.description') }} </span>
        </div>
        <form @submit.prevent="submitForm">
          <input
            v-model="formData.name"
            type="text"
            name="name"
            :placeholder="$t('contactus.form.name')"
          />
          <input
            v-model="formData.tel"
            class="tel"
            type="tel"
            name="tel"
            :placeholder="$t('contactus.form.phone')"
          />
          <input
            v-model="formData.mail"
            class="mail"
            type="email"
            name="mail"
            :placeholder="$t('contactus.form.email')"
          />
        </form>
        <div class="btn">
          <button @click="submitForm">{{ $t('contactus.form.requestbtn') }}</button>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'

const formData = ref({
  name: '',
  tel: '',
  mail: ''
})

function submitForm() {
  console.log('Form data:', formData.value)
}
</script>

<style scoped>
.contact {
  width: auto;
  height: auto;
}

.contact .contact_content {
  width: auto;
  background-image: url('https://images.unsplash.com/photo-1625566360146-918001e76064?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=2670&q=80');
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  padding: 0px 160px;
  position: relative;
  height: 640px;
}

@media (max-width: 878px) {
  .contact .contact_content {
    padding: 0px 80px;
  }
}

@media (max-width: 428px) {
  .contact .contact_content {
    padding: 0px 24px;
  }
}

.contact .contact_form {
  max-width: 560px;
  position: absolute;
  right: 160px;
  padding: 0px 95px;
  backdrop-filter: blur(20px);
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
}

@media (max-width: 878px) {
  .contact .contact_form {
    padding: 0px 40px;
    right: 80px;
  }
}

@media (max-width: 650px) {
  .contact .contact_form {
    width: auto;
    right: 20px;
    left: 20px;
  }
}

.contact .contact_form .title {
  display: flex;
  flex-direction: column;
  margin-bottom: 45px;
}

.contact .contact_form .title .main {
  font-family: 'Montserrat';
  font-style: normal;
  font-weight: 700;
  font-size: 24px;
  line-height: 29px;
  color: #ffffff;
}

.contact .contact_form .title .other {
  font-family: 'Montserrat';
  font-style: normal;
  font-weight: 500;
  font-size: 14px;
  line-height: 17px;
  color: #ffc700;
  background: none;
}

.contact .contact_form form {
  display: flex;
  flex-direction: column;
  width: 360px;
}

@media (max-width: 650px) {
  .contact .contact_form form {
    width: auto;
  }
}

.contact .contact_form input {
  background: none;
  border: none;
  border-bottom: 1px solid #ffffff;
  font-family: 'Montserrat', sans-serif;
  font-style: normal;
  font-weight: 500;
  font-size: 12px;
  line-height: 15px;
  color: #ffffff;
}

.contact .contact_form input::-webkit-input-placeholder {
  color: #ffffff;
}

.contact .contact_form input::-moz-placeholder {
  color: #ffffff;
}

.contact .contact_form input:-moz-placeholder {
  color: #ffffff;
}

.contact .contact_form input:-ms-input-placeholder {
  color: #ffffff;
}

.contact .contact_form .tel {
  margin-top: 45px;
}

.contact .contact_form .mail {
  margin-top: 45px;
}

.contact .contact_form .btn {
  margin-top: 60px;
}

.contact .contact_form .btn button {
  padding: 15px 62px;
  background: linear-gradient(92.71deg, #0499dd 0%, #17c1bc 100%);
  border-radius: 60px;
  border: none;
  font-family: 'Montserrat';
  font-style: normal;
  font-weight: 700;
  font-size: 14px;
  line-height: 17px;
  color: #ffffff;
  cursor: pointer;
  transition: 0.5s ease all;
}

.contact .contact_form .btn button:hover {
  transition: 0.5s ease all;
  background: linear-gradient(92.71deg, #0287c5 0%, #13928e 100%);
}
</style>

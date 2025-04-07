<template>
  <div class="verify-otp-page">
    <h1 class="title">Verify Your Email</h1>
    <p class="subtitle">Enter the 6-digit code we sent to your email.</p>

    <form @submit.prevent="handleVerify">
      <div class="otp-inputs">
        <input
          v-for="(digit, index) in otp"
          :key="index"
          type="text"
          maxlength="1"
          class="otp-box"
          v-model="otp[index]"
          @input="focusNext(index)"
          @keydown.backspace="focusPrev(index, $event)"
        />
      </div>

      <button type="submit" class="verify-btn">Verify</button>
    </form>

    <p class="resend-text">
      Didn’t receive code?
      <a href="#" @click.prevent="resendCode">Resend</a>
    </p>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const otp = ref(['', '', '', '', '', ''])

const handleVerify = () => {
  const code = otp.value.join('')
  if (code.length === 6) {
    console.log('Verifying OTP:', code)
    // Send to backend to verify
  } else {
    alert('Please enter all 6 digits.')
  }
}

const focusNext = (index) => {
  if (otp.value[index].length === 1 && index < 5) {
    const nextInput = document.querySelectorAll('.otp-box')[index + 1]
    nextInput?.focus()
  }
}

const focusPrev = (index, event) => {
  if (!otp.value[index] && index > 0 && event.key === 'Backspace') {
    const prevInput = document.querySelectorAll('.otp-box')[index - 1]
    prevInput?.focus()
  }
}

const resendCode = () => {
  alert('Resend OTP code triggered')
  // Send API call to resend OTP here
}
</script>

<style scoped>
.verify-otp-page {
  max-width: 400px;
  margin: 80px auto;
  text-align: center;
}
.title {
  font-size: 28px;
  font-weight: 600;
}
.subtitle {
  margin: 10px 0 30px;
  color: #666;
}
.otp-inputs {
  display: flex;
  justify-content: space-between;
  gap: 10px;
  margin-bottom: 25px;
}
.otp-box {
  width: 50px;
  height: 60px;
  text-align: center;
  font-size: 24px;
  border: 2px solid #ccc;
  border-radius: 8px;
}
.otp-box:focus {
  border-color: #007bff;
  outline: none;
}
.verify-btn {
  background-color: #007bff;
  color: #fff;
  padding: 12px 0;
  width: 100%;
  border: none;
  border-radius: 8px;
  font-weight: bold;
  font-size: 16px;
  cursor: pointer;
}
.verify-btn:hover {
  background-color: #0056b3;
}
.resend-text {
  margin-top: 20px;
}
.resend-text a {
  color: #007bff;
  text-decoration: underline;
  cursor: pointer;
}
</style>

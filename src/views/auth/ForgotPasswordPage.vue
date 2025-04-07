<template>
    <div class="min-h-screen flex items-center justify-center bg-gray-100 px-4">
      <div class="max-w-md w-full bg-white rounded-xl shadow-md p-8">
        <h2 class="text-2xl font-bold mb-2 text-center text-gray-800">
          Forgot Your Password?
        </h2>
        <p class="text-sm text-gray-500 mb-6 text-center">
          Enter your email and we’ll send you a link to reset your password.
        </p>
  
        <form @submit.prevent="submitForm">
          <div class="mb-4">
            <label for="email" class="block text-sm font-medium text-gray-700 mb-1">
              Email address
            </label>
            <input
              type="email"
              id="email"
              v-model="email"
              class="w-full px-4 py-2 border rounded-lg focus:outline-none focus:ring focus:ring-blue-300"
              placeholder="you@example.com"
            />
            <p v-if="emailError" class="text-sm text-red-500 mt-1">{{ emailError }}</p>
          </div>
  
          <button
            type="submit"
            class="w-full py-2 px-4 bg-blue-600 text-white font-semibold rounded-lg hover:bg-blue-700 transition"
          >
            Send Reset Link
          </button>
        </form>
  
        <div class="mt-4 text-center">
          <router-link to="/login" class="text-blue-500 hover:underline text-sm">
            ⬅ Back to Login
          </router-link>
        </div>
  
        <div v-if="successMessage" class="text-green-600 text-sm mt-4 text-center">
          {{ successMessage }}
        </div>
      </div>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue'
  
  const email = ref('')
  const emailError = ref('')
  const successMessage = ref('')
  
  const validateEmail = (value) => {
    const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/
    return emailRegex.test(value)
  }
  
  const submitForm = () => {
    emailError.value = ''
    successMessage.value = ''
  
    if (!email.value) {
      emailError.value = 'Email is required.'
      return
    }
  
    if (!validateEmail(email.value)) {
      emailError.value = 'Please enter a valid email.'
      return
    }
  
    // Simulate API call
    setTimeout(() => {
      successMessage.value = 'Reset link sent! Check your inbox.'
      email.value = ''
    }, 1000)
  }
  </script>
  
  <style scoped>
  /* Optional custom styles */
  </style>
  
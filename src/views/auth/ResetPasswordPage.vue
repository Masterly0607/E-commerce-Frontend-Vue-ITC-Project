<template>
    <div class="min-h-screen flex items-center justify-center bg-gray-100 px-4">
      <div class="max-w-md w-full bg-white rounded-xl shadow-md p-8">
        <h2 class="text-2xl font-bold mb-2 text-center text-gray-800">
          Reset Password
        </h2>
        <p class="text-sm text-gray-500 mb-6 text-center">
          Enter your new password below.
        </p>
  
        <form @submit.prevent="submitForm">
          <!-- New Password -->
          <div class="mb-4">
            <label for="password" class="block text-sm font-medium text-gray-700 mb-1">
              New Password
            </label>
            <input
              type="password"
              id="password"
              v-model="password"
              class="w-full px-4 py-2 border rounded-lg focus:outline-none focus:ring focus:ring-blue-300"
              placeholder="Enter new password"
            />
          </div>
  
          <!-- Confirm Password -->
          <div class="mb-4">
            <label for="confirmPassword" class="block text-sm font-medium text-gray-700 mb-1">
              Confirm Password
            </label>
            <input
              type="password"
              id="confirmPassword"
              v-model="confirmPassword"
              class="w-full px-4 py-2 border rounded-lg focus:outline-none focus:ring focus:ring-blue-300"
              placeholder="Confirm new password"
            />
            <p v-if="passwordError" class="text-sm text-red-500 mt-1">{{ passwordError }}</p>
          </div>
  
          <button
            type="submit"
            class="w-full py-2 px-4 bg-blue-600 text-white font-semibold rounded-lg hover:bg-blue-700 transition"
          >
            Reset Password
          </button>
        </form>
  
        <div v-if="successMessage" class="text-green-600 text-sm mt-4 text-center">
          {{ successMessage }}
        </div>
  
        <div class="mt-4 text-center">
          <router-link to="/login" class="text-blue-500 hover:underline text-sm">
            ⬅ Back to Login
          </router-link>
        </div>
      </div>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue'
  
  const password = ref('')
  const confirmPassword = ref('')
  const passwordError = ref('')
  const successMessage = ref('')
  
  const submitForm = () => {
    passwordError.value = ''
    successMessage.value = ''
  
    if (!password.value || !confirmPassword.value) {
      passwordError.value = 'Both fields are required.'
      return
    }
  
    if (password.value !== confirmPassword.value) {
      passwordError.value = 'Passwords do not match.'
      return
    }
  
    if (password.value.length < 6) {
      passwordError.value = 'Password must be at least 6 characters.'
      return
    }
  
    // Simulate API call
    setTimeout(() => {
      successMessage.value = 'Password has been reset successfully!'
      password.value = ''
      confirmPassword.value = ''
    }, 1000)
  }
  </script>
  
<template>
    <div>
      
        <!-- Discount section -->
          <section>
      <div class="container-fluid bg-dark py-2">
        <div class="d-flex align-items-center">
        
            
          <div class="flex-grow-1 text-center text-white">
            Summer Sale For All Swim Suits And Free Express Delivery - OFF 50%!
            <router-link class="text-info text-white fw-bold ms-2">ShopNow</router-link>
          </div>
  
          <div class="dropdown">
            <button
              class="btn btn-dark"
              type="button"
              id="dropdownMenuButton1"
              data-bs-toggle="dropdown"
              aria-expanded="false"
            >
              {{ selectedLanguage }}
              <i class="fa-solid fa-chevron-down ps-1"></i>
            </button>
            <ul class="dropdown-menu" aria-labelledby="dropdownMenuButton1">
              <li>
                <a class="dropdown-item" href="#english" @click.prevent="isSelectedLaguage('English')">English</a>
              </li>
              <li>
                <a class="dropdown-item" href="#khmer" @click.prevent="isSelectedLaguage('Khmer')">Khmer</a>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </section>

    <!-- Navbar -->
     <section class="text-center">
        <div class="container bg-white">
            <nav class="navbar navbar-expand-lg navbar-white bg-white p-3  ">

  <div class="container-fluid">
    <a class="navbar-brand" href="#">ITC Shop</a>
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarSupportedContent">
      <ul class="navbar-nav ms-auto mb-2 mb-lg-0">
        <li class="nav-item">
          <a class="nav-link active" aria-current="page" href="#">Home</a>
        </li>
        <li class="nav-item">
          <a class="nav-link" href="#">Link</a>
        </li>
       
      
      </ul>
     
      <q-input dark borderless v-model="text" :readonly="readonly" :disable="disable">
        <template v-slot:append>
          <q-icon name="search" />
        </template>
      </q-input>


    </div>
  </div>
</nav>
        </div>
     </section>
    </div>
    <div>
    <label for="price" class="block text-sm/6 font-medium text-gray-900">Price</label>
    <div class="mt-2">
      <div class="flex items-center rounded-md bg-white pl-3 outline-1 -outline-offset-1 outline-gray-300 has-[input:focus-within]:outline-2 has-[input:focus-within]:-outline-offset-2 has-[input:focus-within]:outline-indigo-600">
        <div class="shrink-0 text-base text-gray-500 select-none sm:text-sm/6">$</div>
        <input type="text" name="price" id="price" class="block min-w-0 grow py-1.5 pr-3 pl-1 text-base text-gray-900 placeholder:text-gray-400 focus:outline-none sm:text-sm/6" placeholder="0.00" />
        <div class="grid shrink-0 grid-cols-1 focus-within:relative">
          <select id="currency" name="currency" aria-label="Currency" class="col-start-1 row-start-1 w-full appearance-none rounded-md py-1.5 pr-7 pl-3 text-base text-gray-500 placeholder:text-gray-400 focus:outline-2 focus:-outline-offset-2 focus:outline-indigo-600 sm:text-sm/6">
            <option>USD</option>
            <option>CAD</option>
            <option>EUR</option>
          </select>
          <ChevronDownIcon class="pointer-events-none col-start-1 row-start-1 mr-2 size-5 self-center justify-self-end text-gray-500 sm:size-4" aria-hidden="true" />
        </div>
      </div>
    </div>
  </div>
  
  </template>
  
  <script setup>
import { ChevronDownIcon } from '@heroicons/vue/16/solid'
  import { ref } from 'vue'
  const selectedLanguage = ref('English')
  const isSelectedLaguage = (lang) => {
    selectedLanguage.value = lang
  }
  </script>
  
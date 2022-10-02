<template>
  <header class=" border-b-2 border-indigo-100 bg-white">
    <div class=" flex justify-between m-6 ">
      <Logo />
      <RouterLink to="/login">
        <button class=" bg-violet-500 border-2 border-violet-700 rounded-lg drop-shadow-md hover:bg-violet-700">
          <p class="py-2 px-3 font-lato text-Extended/true-gray/50 text-[12px] drop-shadow-md md:text-base lg:text-lg">
            Login</p>
        </button>
      </RouterLink>
    </div>
    <nav>
      <div>
        <ul class="hidden flex-auto justify-center gap-6 sm:flex">
          <li>
            <router-link class="hover:font-bold" to="/">Home </router-link>
          </li>
          <li>
            <router-link class="hover:font-bold" to="/simple">Page Simple </router-link>
          </li>
          <li>
            <router-link class="hover:font-bold" to="/liste">Liste </router-link>
          </li>
          <li>
            <router-link class="hover:font-bold" to="/liste-fetch">Liste Fetch </router-link>
          </li>
          <li>
            <router-link class="hover:font-bold" to="/edit/new">Formulaire pour créer un offre</router-link>
          </li>
          <li>
            <router-link class="hover:font-bold" to="/list-supabase">Liste Supabase</router-link>
          </li>
          <li>
            <router-link class="hover:font-bold" to="/edit/id">Test - Editer une offre</router-link>
          </li>
        </ul>
      </div>
    </nav>
  </header>

  <Suspense>
    <router-view class="m-2 border-5" />
  </Suspense>

  <!-- Affiche les pages -->
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/@iconscout/unicons@3.0.6/css/line.css">


  <footer class="bg-white pt-10 sm:mt-10">
    <div>
      <Logo class=" mt-12 ml-6"></Logo>
    </div>
    <div class="max-w-6xl m-auto text-gray-900 flex flex-wrap justify-left">

      <div class="p-5 w-1/2 sm:w-4/12 md:w-3/12">

        <div class="text-xs uppercase text-gray-900 font-bold mb-6">
          SELL A HOME
        </div>


        <a href="#" class="my-3 block text-gray-500 hover:text-gray-100 text-sm font-normal duration-700">
          Request an offer
        </a>
        <a href="#" class="my-3 block text-gray-500 hover:text-gray-100 text-sm  font-normal duration-700">
          Pricing
        </a>
        <a href="#" class="my-3 block text-gray-500 hover:text-gray-100 text-sm  font-normal duration-700">
          Reviews
        </a>
        <a href="#" class="my-3 block text-gray-500 hover:text-gray-100 text-sm  font-normal duration-700">
          Stories
        </a>
      </div>


      <div class="p-5 w-1/2 sm:w-4/12 md:w-3/12">

        <div class="text-xs uppercase text-gray-900 font-bold mb-6">
          TERMS & PRIVACY
        </div>


        <a href="#" class="my-3 block text-gray-500 hover:text-gray-100 text-sm  font-normal duration-700">
          Trust & Safety
        </a>
        <a href="#" class="my-3 block text-gray-500 hover:text-gray-100 text-sm  font-normal duration-700">
          Terms of Service
        </a>
        <a href="#" class="my-3 block text-gray-500 hover:text-gray-100 text-sm  font-normal duration-700">
          Privacy Policy
        </a>
      </div>

      <div class="p-5 w-1/2 sm:w-4/12 md:w-3/12">
        <div class="text-xs uppercase text-gray-900 font-bold mb-6">
          BUY A HOME
        </div>

        <a href="#" class="my-3 block text-gray-500 hover:text-gray-100 text-sm  font-normal duration-700">
          Buy
        </a>
        <a href="#" class="my-3 block text-gray-500 hover:text-gray-100 text-sm  font-normal duration-700">
          Finance
        </a>
      </div>

      <div class="p-5 w-1/2 sm:w-4/12 md:w-3/12">
        <div class="text-xs uppercase text-gray-900 font-bold mb-6">
          ABOUT
        </div>

        <a href="#" class="my-3 block text-gray-500 hover:text-gray-100 text-sm  font-normal duration-700">
          Company
        </a>
        <a href="#" class="my-3 block text-gray-500 hover:text-gray-100 text-sm  font-normal duration-700">
          How it works
        </a>
        <a href="#" class="my-3 block text-gray-500 hover:text-gray-100 text-sm  font-normal duration-700">
          Contact
        </a>
        <a href="#" class="my-3 block text-gray-500 hover:text-gray-100 text-sm  font-normal duration-700">
          Investors
        </a>
      </div>


      <div class="p-5 w-1/2 sm:w-4/12 md:w-3/12">

        <div class="text-xs uppercase text-gray-900 font-bold mb-6">
          BUY, RENT AND SELL
        </div>


        <a href="#" class="my-3 block text-gray-500 hover:text-gray-100 text-sm  font-normal   duration-700">
          Builder trade-up
        </a>
        <a href="#" class="my-3 block text-gray-500 hover:text-gray-100 text-sm  font-normal duration-700">
          Rent home
        </a>
        <a href="#" class="my-3 block text-gray-500 hover:text-gray-100 text-sm  font-normal   duration-700">
          Builder trade-up
        </a>
      </div>

      <div class="p-5 w-1/2 sm:w-4/12 md:w-3/12">
        <div class="text-xs uppercase text-gray-900 font-bold mb-6">
          RESOURCES
        </div>

        <a href="#" class="my-3 block text-gray-500 hover:text-gray-100 text-sm font-normal duration-700">
          Blog
        </a>
        <a href="#" class="my-3 block text-gray-500 hover:text-gray-100 text-sm  font-normal  duration-700">
          Guides
        </a>
        <a href="#" class="my-3 block text-gray-500 hover:text-gray-100 text-sm  font-normal  duration-700">
          FAQ
        </a>
        <a href="#" class="my-3 block text-gray-500 hover:text-gray-100 text-sm  font-normal duration-700">
          Help Center
        </a>
      </div>

    </div>


    <div class="pt-2">
      <div class="flex pb-5 px-3 m-auto pt-5 
            border-t border-indigo-100 text-gray-900 text-sm 
            flex-col md:flex-row max-w-6xl">
        <div class="mt-2 text-center">
          ©2021 Estatery. All rights reserved
        </div>
        <div class="mt-6 flex-row flex justify-center">
          <a href="#" class="w-6 mx-1">
            <i class="uil uil-facebook-f"></i>
          </a>
          <a href="#" class="w-6 mx-1">
            <i class="uil uil-twitter-alt"></i>
          </a>
          <a href="#" class="w-6 mx-1">
            <i class="uil uil-linkedin"></i>
          </a>
          <a href="#" class="w-6 mx-1">
            <i class="uil uil-instagram"></i>
          </a>
        </div>
      </div>
    </div>
  </footer>

</template>

<script setup lang="ts">
import Logo from './components/icones/Logo.vue'
import Navigation from './components/icones/Navbar.vue'
</script>

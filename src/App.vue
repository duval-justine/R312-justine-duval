<template>
  <header class=" border-b-2 border-indigo-100 bg-white">
    <div class=" flex justify-between m-6 ">
      <Logo />
      <Navigation class="h-5 w-5" />
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
        </ul>
      </div>

    </nav>
  </header>

  <Suspense>
    <router-view class="m-2 border-5" />
  </Suspense>
  <!-- Affiche les pages -->
  <router-view class="m-2 border-2 p-2" />
</template>

<script setup lang="ts">
import { Bars3Icon } from '@heroicons/vue/20/solid'
import Logo from './components/icones/Logo.vue'
import Navigation from './components/icones/Navbar.vue'
</script>

<script setup lang="ts">
import AfficheMaison from "../components/AfficheMaison.vue"
    const dataMaisons = [{
        titre:"Palm Harbor",
         price:2095, 
         favoris:true,
          lieu:"2699 Green Valley, Highland Lake ", 
          nbrSDB:2, 
          image:"/images-maison/maison2.jpg"
        
    }];
</script>

<template>
    <div class="p-2">
        <h2>Page Simple</h2>
        <div class="grid grid-flow-row-dense grid-cols-[repeat(auto-fit,minmax(343px,1fr))]">
            <div v-for="dataMaison in dataMaisons" :key="dataMaison.price"><AfficheMaison  v-bind="dataMaison"/></div>
            
           
            
        </div>
    </div>
</template>
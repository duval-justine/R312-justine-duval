<script setup lang="ts">
    import AfficheMaison from "../components/AfficheMaison.vue"
    const dataMaison0 = {
        titre:"Palm Harbor",
         price:2095, 
         favoris:true,
          lieu:"2699 Green Valley, Highland Lake ", 
          nbrSDB:2, 
          image:"/images-maison/maison2.jpg"
          };
    const dataMaison1 = {
        titre:"Faulkner Ave",
         price:4550, 
         favoris:false,
          lieu:"909 Woodland St, Michigan, IN", 
          nbrSDB:3, 
          image:"/images-maison/maison3.jpg"
          };
</script>

<template>
    <div class="p-2">
        <h2>Page Simple</h2>
        <div class="grid grid-flow-row-dense grid-cols-[repeat(auto-fit,minmax(343px,1fr))]">
            <AfficheMaison class="p-4"  v-bind="dataMaison0"/>
            <AfficheMaison class="p-4"  v-bind="dataMaison1"/>
        </div>
    </div>
</template>
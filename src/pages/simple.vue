<script setup lang="ts">
import AfficheMaison from "../components/AfficheMaison.vue"
const dataMaison0 = {
    titre: "Beverly Springfield",
    price: 1723,
    favoris: true,
    lieu: "2821 Lake Sevilla, Palm Harbor, TX",
    nbrSDB: 2,
    nbrChambres: 2,
    surface: 150,
    image: "/images-maison/maison1.jpg"
};
const dataMaison1 = {
    titre: "Palm Harbor",
    price: 2095,
    favoris: true,
    lieu: "2699 Green Valley, Highland Lake ",
    nbrSDB: 2,
    nbrChambres: 6,
    surface: 500,
    image: "/images-maison/maison2.jpg"
};
const dataMaison2 = {
    titre: "Faulkner Ave",
    price: 4550,
    favoris: false,
    lieu: "909 Woodland St, Michigan, IN",
    nbrSDB: 3,
    nbrChambres: 3,
    surface: 145,
    image: "/images-maison/maison3.jpg"
};
</script>

<template>
    <div class="p-2">
        <h2 class="text-3xl font-bold text-indigo-1000 text-center pt-[3.625rem] mb-8">Page Simple </h2>
        <div class="grid grid-flow-row-dense grid-cols-[repeat(auto-fit,minmax(343px,1fr))]">
            <AfficheMaison class="p-4" v-bind="dataMaison0" />
            <AfficheMaison class="p-4" v-bind="dataMaison1" />
            <AfficheMaison class="p-4" v-bind="dataMaison2" />
        </div>
    </div>
</template>
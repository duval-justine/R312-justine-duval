<script setup lang="ts">
import AfficheMaison from "../components/AfficheMaison.vue"
const dataMaisons = [{ titre: "Beverly Springfield", price: 1723, favoris: true, lieu: "2821 Lake Sevilla, Palm Harbor, TX", nbrSDB: 2, nbrChambres: 5, surface: 320, image: "/images-maison/maison1.jpg" },
{ titre: "Palm Harbor", price: 2095, favoris: false, lieu: "2699 Green Valley, Highland Lake ", nbrSDB: 2, nbrChambres: 2, surface: 150, image: "/images-maison/maison2.jpg" },
{ titre: "Faulkner Ave", price: 4550, favoris: false, lieu: "909 Woodland St, Michigan, IN", nbrSDB: 3, nbrChambres: 6, surface: 400, image: "/images-maison/maison3.jpg" },
{ titre: "St. Christal", price: 4650, favoris: true, lieu: "210 US Highway, HighlandLake, FL", nbrSDB: 2, nbrChambres: 3, surface: 250, image: "/images-maison/maison4.jpg" },
{ titre: "Cover Red", price: 3100, favoris: false, lieu: "243 CurlewRoad, PalmHarbor, TX", nbrSDB: 2, nbrChambres: 2, surface: 100, image: "/images-maison/maison5.jpg" },
{ titre: "Tarpon Bay", price: 4800, favoris: true, lieu: "103 Lake Shores, Michigan, IN", nbrSDB: 3, nbrChambres: 4, surface: 230, image: "/images-maison/maison6.jpg" },
];
</script>

<template>
    <div class="p-2">
        <h2 class="text-3xl font-bold text-indigo-1000 text-center pt-[3.625rem] mb-8">Liste </h2>
        <div class="grid grid-flow-row-dense grid-cols-[repeat(auto-fit,minmax(343px,1fr))]">
            <div class="p-4" v-for="dataMaison in dataMaisons" :key="dataMaison.titre">
                <AfficheMaison v-bind="dataMaison" />
            </div>



        </div>
    </div>
</template>
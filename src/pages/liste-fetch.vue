<script setup lang="ts">
import AfficheMaison from "../components/AfficheMaison.vue";
const res = await fetch("maisons.json");
const dataMaisons = await res.json();
</script>

<template>
    <div class="p-5">
        <h2 class="text-3xl font-bold text-indigo-1000 text-center pt-[3.625rem] mb-8">Liste Fetch </h2>
        <div class="grid grid-flow-row-dense grid-cols-[repeat(auto-fit,minmax(343px,1fr))]">
            <div class="p-4" v-for="dataMaison in dataMaisons" :key="dataMaison.nom">
                <AfficheMaison v-bind="dataMaison" />
            </div>
        </div>
    </div>
</template>


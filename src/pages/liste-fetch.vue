<script setup lang="ts">
import AfficheMaison from "../components/AfficheMaison.vue";
const res = await fetch("maisons.json");
const dataMaisons = await res.json();
</script>

<template>
    <div class="p-5">
        <h1>Page Liste fetch</h1>
        <div class="grid grid-flow-row-dense grid-cols-[repeat(auto-fit,minmax(343px,1fr))]">
            <div class="p-4" v-for="dataMaison in dataMaisons" :key="dataMaison.nom">
                <AfficheMaison v-bind="dataMaison" />
            </div>
        </div>
    </div>
</template>


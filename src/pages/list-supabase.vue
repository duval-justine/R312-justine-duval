<script setup lang="ts">
import { supabase } from "../supabase";
console.log("supabase :", supabase); // pour vérifier et "garder" supabase dans le code
const maisons = []; // à remplacer par l'appel à Supabase
</script>

<template>
    <div class="p-5">
        <h2 class="text-3xl font-bold text-indigo-1000 text-center pt-[3.625rem] mb-8">Liste des maisons de Supabase
        </h2>
        <div class="grid grid-flow-row-dense grid-cols-[repeat(auto-fit,minmax(343px,1fr))]">
            <div class="p-4" v-for="dataMaison in dataMaisons" :key="dataMaison.nom">
                <AfficheMaison v-bind="dataMaison" />
            </div>
        </div>
    </div>
</template>


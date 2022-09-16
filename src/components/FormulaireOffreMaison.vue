<script setup lang="ts">
import { ref } from "@vue/reactivity";
import AfficheMaison from "./AfficheMaison.vue";
const dataMaison = ref({});
</script>

<template>
    <div>
        <div class="p-2">
            <h2 class="text-2xl">Résultat (Prévisualisation)</h2>
            <AfficheMaison v-bind="dataMaison" />
        </div>
        <div class="p-2">
            <FormKit type="form" v-model="dataMaison">
                <FormKit name="titre" label="Nom de la maison" />
                <FormKit name="price" label="Prix de la maison" type="number" />
                <FormKit name="favoris" label="Favoris" type="checkbox" />
                <FormKit name="lieu" label="Adresse de la maison" />
                <FormKit name="nbrSDB" label="Nombre de salle de bain" type="number" />
            </FormKit>
        </div>
    </div>
</template>
<script setup lang="ts">
import { ref } from "@vue/reactivity";
import AfficheMaison from "./AfficheMaison.vue";
const dataMaison = ref({});
</script>

<template>
    <div>
        <div class="p-2">
            <h2 class="text-2xl mb-4">Prévisualisation :</h2>
            <AfficheMaison v-bind="dataMaison" />
        </div>
        <div class="p-2">
            <FormKit type="form" :submit-attrs="{ classes: {input: 'bg-indigo-100 hover:bg-indigo-200 rounded p-2'}}"
                :config="{ classes: {input: 'border-gray-300 p-1 rounded shadow-sm border'}}" v-model="dataMaison">
                <div class="mb-2">
                    <FormKit name="titre" label="Nom de la maison" />
                </div>
                <div class="mb-2">
                    <FormKit name="price" label="Prix de la maison" type="number" />
                </div>
                <div class="mb-2">
                    <FormKit name="favoris" label="Ajouter aux favoris" type="checkbox" wrapper-class="flex" />
                </div>
                <FormKit name="lieu" label="Adresse de la maison" />
                <div class="mb-8">
                    <FormKit name="nbrSDB" label="Nombre de salle de bain" type="number" />
                </div>
            </FormKit>
        </div>
    </div>
</template>
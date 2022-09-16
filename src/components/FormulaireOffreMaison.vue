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
                <FormKit name="titre" label="nom" />
                <FormKit name="price" label="prix" type="number" />
                <FormKit name="favoris" label="mettre en valeur" type="checkbox" />
                <FormKit name="lieu" label="name" />
                <FormKit name="nombre de salle de bain" label="number" type="number" />
            </FormKit>
        </div>
    </div>
</template>
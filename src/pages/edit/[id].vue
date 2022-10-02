<script setup lang="ts">
import FormulaireOffreMaison from "../../components/FormulaireOffreMaison.vue"
defineProps(["id"]);
</script>
            
<template>
    <div class="p-2">
        <h2 class="text-3xl font-bold text-indigo-1000 text-center pt-[3.625rem] mb-8">Formulaire pour éditer une offre
        </h2>
        <div class="grid grid-flow-row-dense grid-cols-[repeat(auto-fit,minmax(343px,1fr))]">
            <FormulaireOffreMaison />
        </div>
    </div>
</template>
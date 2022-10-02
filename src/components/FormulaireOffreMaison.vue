<script setup lang="ts">
import { ref } from "@vue/reactivity";
import AfficheMaison from "./AfficheMaison.vue";
import { supabase } from "../supabase";
const dataMaison = ref({});

// On fait une variable réactive qui réference les données
// ATTENTION : faire une Ref pas une Reactive car :
// c'est l'objet qui doit être réactif, pas ses props


import { useRouter } from "vue-router";
const router = useRouter();
const props = defineProps(["id"]);
if (props.id) {
    // On charge les données de la maison
    let { data, error } = await supabase
        .from("maison")
        .select("*")
        .eq("id", props.id);
    if (error) console.log("n'a pas pu charger le table Maison :", error);
    else dataMaison.value = (data as any[])[0];
}
async function upsertMaison(dataForm, node) {
    const { data, error } = await supabase.from("maison").upsert(dataForm);
    if (error) node.setErrors([error.message]);
    else {
        node.setErrors([]);
        router.push({ name: "edit-id", params: { id: data[0].id } });
    }


}


</script>

<template>
    <div>
        <div class="p-2">
            <h2 class="text-2xl mb-4">Prévisualisation :</h2>
            <AfficheMaison v-bind="dataMaison" />
        </div>
        <div class="p-2">
            <FormKit type="form" :submit-attrs="{ classes: {input: 'bg-indigo-100 hover:bg-indigo-200 rounded p-2'}}"
                :config="{ classes: {input: 'border-gray-300 p-1 rounded shadow-sm border'}}" v-model="dataMaison"
                @submit="upsertMaison">
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


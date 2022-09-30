<script setup lang="ts">
import { ref } from "@vue/reactivity";
import { supabase, user } from "../supabase";
async function signIn(data, node) {
    const { user, error } = await (nvlUtilisateur.value
        ? supabase.auth.signUp(data)
        : supabase.auth.signIn(data));
    if (error) {
        console.error(error);
        node.setErrors([error.message]);
    }
}
const nvlUtilisateur = ref(false);
</script>
<template>
    <div class="flex justify-center">
        <button class="mt-4 bg-violet-300 border-violet-500 hover:bg-violet-500 rounded p-2" v-if="user"
            @pointerdown="supabase.auth.signOut()">
            Se déconnecter ({{ user.email }})
        </button>
        <FormKit v-else type="form"
            :submit-attrs="{ classes: {input: 'mt-4 bg-violet-300 border-violet-500 hover:bg-violet-500 rounded p-2'}}"
            :submit-label="nvlUtilisateur ? 'S inscrire' : 'Se connecter'" @submit="signIn">
            <div class="mt-32 mb-8">
                <FormKit name="email" :config="{ classes: {input: 'border-gray-300 p-1 rounded shadow-sm border'}}"
                    label="Votre adresse mail" type="email" />
            </div>
            <div class="mb-2">
                <FormKit name="password" :config="{ classes: {input: 'border-gray-300 p-1 rounded shadow-sm border'}}"
                    label="Mot de passe" type="password" />
                <formKit label="Nouvel utilisateur ?"
                    :submit-attrs="{ classes: {input: 'mt-4 bg-violet-300 border-violet-500 hover:bg-violet-500 rounded p-2'}}"
                    name="nvlUtilisateur" type="checkbox" v-model="nvlUtilisateur" />
            </div>
        </FormKit>
    </div>
</template>
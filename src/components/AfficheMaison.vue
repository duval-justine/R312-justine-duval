<script setup lang="ts">
import bed from "./icones/Bed.vue"
import bath from "./icones/Bath.vue"
import dimension from "./icones/Dimension.vue"
import heart from "./icones/Heart.vue"

defineProps({
    price: {
        type: Number,
        default: 2700,
    },
    favoris: {
        type: Boolean,
        default: false,
    },
    titre: {
        type: String,
        required: true
    },
    image: String,
    surface: String,
    nbrSDB: Number,
    nbrChambres: Number,
    lieu: String,
},
);
</script>

<template>
    <figure>
        <img class="rounded-t-lg" :src="image" alt="">
        <figcaption class="flex flex-col relative px-5 py-7 border-2 border-t-0 rounded-b-lg">
            <h3 class="text-2xl text-gray-900 font-bold">{{titre}}</h3>
            <address class="not-italic text-gray-500">{{ lieu }}</address>
            <div class="order-first flex items-center">
                <div class="text-2xl text-indigo-500 font-bold">${{ price.toLocaleString("en-US") }}</div>
                <div class="text-gray-500 ">/month</div>
            </div>
            <hr class="border-indigo-100 border-t-2 my-2" />
            <div class="flex justify-between text-sm">
                <div>
                    <bed class="inline-block align-top" /> {{nbrChambres}} Beds
                </div>
                <div>
                    <bath class="inline-block align-top" /> {{ nbrSDB }} Bathrooms
                </div>
                <div>
                    <dimension class="inline-block align-top" /> {{surface}} m²
                </div>
            </div>
            <div
                class="grid place-items-center w-12 h-12 border-2 border-indigo-100 rounded-full absolute top-7 right-5">
                <heart :class="{'fill-indigo-500': favoris}" />
            </div>
        </figcaption>
    </figure>
</template>

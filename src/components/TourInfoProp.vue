<template>
    <div class="flex gap-40 py-8">
        <!-- Date Section -->
        <div class="">
            <p class="text-white text-5xl font-bold">{{ date }}</p>
            <p class="text-white text-5xl font-bold">{{ month }}</p>
        </div>

        <!-- Location Section -->
        <div class="">
            <h1 class="text-white text-4xl font-bold">{{ location }}</h1>
            <p class="text-white">{{ city }}</p>
        </div>

        <!-- Action Buttons -->
        <div class="flex flex-col justify-center items-center">
            <div class="bg-white px-12 py-3 text-center text-xl font-semibold rounded">
                BUY TICKETS
            </div>
            <div class="flex">
                <p class="text-white">Learn More</p>
                <img src="" alt="learn more">
            </div>
        </div>
    </div>
</template>

<script setup>
import { defineProps } from 'vue';
defineProps({  // Fixed syntax: removed curly brace, added parentheses
    date: {
        type: Number,
        required: true  // Added required if these props are mandatory
    },
    month: {
        type: String,
        required: true
    },
    location: {
        type: String,
        required: true
    },
    city: {
        type: String,
        required: true
    }
})
</script>


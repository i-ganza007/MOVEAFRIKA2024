<template>
    <section class="bg-black h-dvh flex items-center py-20 justify-between pr-4 pb-20">
        <div class="h-[120%]">
            <img src="../assets/star.png" alt="" class="h-full">
        </div>
        <div class="flex flex-col self-start mb-5 gap-9">
            <h1 class="text-3xl font-bold text-white text-5xl"><span class="text-red-500">2025 </span>TOUR</h1>
            <div>
                <div class="flex flex-col gap-9 mt-8">
                    <TourInfoProp 
                        :date="kigaliTour.date"
                        :month="kigaliTour.month"
                        :location="kigaliTour.location"
                        :city="kigaliTour.city"
                    />

                    <hr style="background-color: white;">
                    
                    <TourInfoProp 
                        :date="lagosTour.date"
                        :month="lagosTour.month"
                        :location="lagosTour.location"
                        :city="lagosTour.city"
                    />
                </div>
            </div>
        </div>
    </section>
</template>

<script setup>
import TourInfoProp from './TourInfoProp.vue';
import { reactive } from 'vue';

const kigaliTour = reactive({
    date: 21,
    month: 'FEB',
    location: 'BK ARENA',
    city: 'KIGALI, RWANDA'
});

const lagosTour = reactive({
    date: 25,
    month: 'FEB',
    location: 'THE PALMS',
    city: 'LAGOS, NIGERIA'
});
</script>


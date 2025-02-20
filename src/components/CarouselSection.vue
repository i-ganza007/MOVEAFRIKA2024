<template>
    <section class="bg-black flex flex-col gap-7 py-10">
        <div class="text-white text-4xl font-bold mx-auto">MOVE AFRIKA 2023</div>

        <div class="overflow-hidden bg-black py-16">
            <div class="container mx-auto relative">
                <!-- Carousel Container -->
                <div class="relative overflow-hidden">
                    <!-- Sliding Track -->
                    <div class="flex transition-transform duration-500 ease-in-out"
                         :style="{ transform: `translateX(${-currentIndex * 100}%)` }">
                        <!-- All Images in a row -->
                        <div v-for="(image, index) in images" :key="index" 
                             class="flex-shrink-0 w-full flex justify-center gap-4">
                            <!-- Left Image -->
                            <div class="w-1/6">
                                <img :src="require(`../assets/${getPrevImage(index)}`)" 
                                     alt="Left car" 
                                     class="w-full h-[500px] object-cover opacity-50">
                            </div>
                            
                            <!-- Center Image -->
                            <div class="w-4/6">
                                <img :src="require(`../assets/${image}`)" 
                                     alt="Center car" 
                                     class="w-full h-[500px] object-cover">
                            </div>
                            
                            <!-- Right Image -->
                            <div class="w-1/6">
                                <img :src="require(`../assets/${getNextImage(index)}`)" 
                                     alt="Right car" 
                                     class="w-full h-[500px] object-cover opacity-50">
                            </div>
                        </div>
                    </div>

                    <!-- Navigation Buttons -->
                    <button 
                        class="bg-gray-400 w-10 py-2 rounded absolute bottom-70 left-5 hover:bg-gray-500 cursor-pointer z-10" 
                        @click="clickPrev"
                    >
                        <img src="../assets/backwards.png" alt="" class="h-6 mx-auto">
                    </button>
                    
                    <button 
                        class="bg-gray-400 w-10 py-2 rounded absolute bottom-70 right-5 hover:bg-gray-500 cursor-pointer z-10" 
                        @click="clickNext"
                    >
                        <img src="../assets/icons8-arrow-50.png" alt="" class="h-6 mx-auto">
                    </button>
                </div>
            </div>
        </div>

        <div class="bg-white w-32 py-3 px-5 text-center font-bold rounded mx-auto">
            Learn More
        </div>
    </section>
</template>

<script setup>
import { ref } from "vue";

const images = ref(['Car1.jpg', 'Car2.jpg', 'Car3.jpg', 'Car4.jpg', 'Car5.jpg', 'Car6.jpg']);
const currentIndex = ref(0);

const getPrevImage = (index) => {
    const prevIndex = index === 0 ? images.value.length - 1 : index - 1;
    return images.value[prevIndex];
};

const getNextImage = (index) => {
    const nextIndex = index === images.value.length - 1 ? 0 : index + 1;
    return images.value[nextIndex];
};

const clickNext = () => {
    currentIndex.value = (currentIndex.value + 1) % images.value.length;
};

const clickPrev = () => {
    currentIndex.value = currentIndex.value === 0 
        ? images.value.length - 1 
        : currentIndex.value - 1;
};
</script>

<style scoped>
/* Optional: Add smooth scrolling behavior */
.smooth-scroll {
    scroll-behavior: smooth;
}
</style>
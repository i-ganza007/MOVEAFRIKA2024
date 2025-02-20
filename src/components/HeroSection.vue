<template>
    <section :style="{ 
        backgroundImage: `url(${require('@/assets/image-tempo.jpeg')})`,
        backgroundPosition: 'center',
        backgroundRepeat: 'no-repeat',
        backgroundSize: '100%'  // Add this line
    }" class="h-dvh bg-gray-100"> <!-- Added bg-gray-100 to see the container bounds -->
        <div class="flex flex-col items-center justify-center h-full gap-20">
            <img :src="require('@/assets/image.png')" alt="hero" class="w-[480px]">
            <h2 class="text-lg text-white border-b-2 py-5 px-14 font-semibold hover:bg-white hover:text-black">TICKETS NOW ON SALE</h2>
        </div>
    </section>
</template>

<style scoped>
section {
    /* Optional: if you want to ensure the background doesn't tile */
    background-color: #f3f4f6; /* Light gray background */
}
</style>
<template>
    <section>
        <nav class="bg-black flex justify-between px-10 pt-7 h-23 fixed top-0 z-[9999] w-full">
            <div class="w-20">
                <img src="../assets/navbar.png" alt="" class="w-full">
            </div>

            <div class="flex items-center gap-20">
                <ul class="text-white text-lg flex gap-10">
                    <li class="cursor-pointer hover:text-gray-300 transition-colors">TOUR</li>
                    <li class="cursor-pointer hover:text-gray-300 transition-colors">ABOUT</li>
                    <li class="cursor-pointer hover:text-gray-300 transition-colors">NEWS</li>
                    <li class="cursor-pointer hover:text-gray-300 transition-colors">CONTACT</li>
                </ul>

                <!-- Uncomment and style social icons -->
                <!-- <ul class="flex gap-6 items-center">
                    <li class="cursor-pointer hover:opacity-80 transition-opacity">
                        <img src="../assets/insta.png" alt="Instagram" class="w-6 h-6">
                    </li>
                    <li class="cursor-pointer hover:opacity-80 transition-opacity">
                        <img src="../assets/twitter.png" alt="Twitter" class="w-6 h-6">
                    </li>
                    <li class="cursor-pointer hover:opacity-80 transition-opacity">
                        <img src="../assets/tiktok.png" alt="TikTok" class="w-6 h-6">
                    </li>
                    <li class="cursor-pointer hover:opacity-80 transition-opacity">
                        <img src="../assets/facebook.png" alt="Facebook" class="w-6 h-6">
                    </li>
                </ul> -->
            </div>
        </nav>
    </section>
</template>

<style scoped>
/* Optional: Add a background blur effect */
nav {
    backdrop-filter: blur(5px);
    -webkit-backdrop-filter: blur(5px);
}
</style>
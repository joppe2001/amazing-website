<template>
    <header class="header bg-white shadow-md absolute w-screen">
        <div class="container mx-auto px-6 py-4 flex justify-between items-center">
            <a href="#" class="text-xl font-bold text-gray-800">BrandName</a>
            <!-- Desktop Menu -->
            <div class="hidden md:flex space-x-4 desktop-menu">
                <nuxt-link to="/" class="text-gray-600 hover:text-gray-800">Home</nuxt-link>
                <a href="#" class="text-gray-600 hover:text-gray-800">About</a>
                <nuxt-link to="/service/service-page" class="text-gray-600 hover:text-gray-800">Services</nuxt-link>
                <a href="#" class="text-gray-600 hover:text-gray-800">Contact</a>
            </div>
            <!-- Mobile menu button -->
            <button @click="toggleMenu" class="md:hidden focus:outline-none focus:border-gray-300">
                <svg :class="{ 'spin-animation': spinning }" class="w-8 h-6 absolute right-5 top-5" fill="none"
                    stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
                    <path v-if="!openMenu" strokeLinecap="round" strokeLinejoin="round" strokeWidth="2"
                        d="M4 6h16M4 12h16m-7 6h7"></path>
                    <path v-if="openMenu" strokeLinecap="round" strokeLinejoin="round" strokeWidth="2"
                        d="M6 18L18 6M6 6l12 12"></path>
                </svg>
            </button>
        </div>
        <!-- Mobile menu -->
        <div v-if="openMenu"
            class="mobile-menu md:hidden container mx-auto px-6 py-2 mt-3 absolute right-0 rounded shadow-lg bg-white">
            <nuxt-link to="/" @click="openMenu = !openMenu"
                class="block py-2 px-4 text-gray-600 hover:text-gray-800 text-right">Home</nuxt-link>
            <nuxt-link to="" @click="openMenu = !openMenu"
                class="block py-2 px-4 text-gray-600 hover:text-gray-800 text-right">About</nuxt-link>
            <nuxt-link to="/service/service-page" @click="openMenu = !openMenu"
                class="block py-2 px-4 text-gray-600 hover:text-gray-800 text-right">Services</nuxt-link>
            <nuxt-link to="" @click="openMenu = !openMenu"
                class="block py-2 px-4 text-gray-600 hover:text-gray-800 text-right">Contact</nuxt-link>
        </div>
    </header>
</template>

<script setup>
import { ref } from 'vue'

const openMenu = ref(false)
const spinning = ref(false)

const toggleMenu = () => {
    spinning.value = true
    setTimeout(() => {
        openMenu.value = !openMenu.value
        spinning.value = false
    }, 300) // 500ms is the duration of the spin animation
}
</script>

<style scoped>
/* Slide down when menu opens */
.mobile-menu {
    animation: slideDown 0.3s ease-in-out forwards;
}

/* Slide up when menu closes */
.mobile-menu[aria-hidden="true"] {
    animation: slideUp 0.3s ease-in-out forwards;
}

/* Spin animation */
.spin-animation {
    animation: spin 0.3s ease-in-out;
}

@keyframes spin {
    0% {
        transform: rotate(0deg);
        opacity: 1;
    }

    100% {
        transform: rotate(360deg);
        opacity: 0;
    }
}

@keyframes slideDown {
    0% {
        transform: translateY(-20%);
        opacity: 0;
    }

    100% {
        transform: translateY(0);
        opacity: 1;
    }
}

@keyframes slideUp {
    0% {
        transform: translateY(0);
        opacity: 1;
    }

    100% {
        transform: translateY(-20%);
        opacity: 0;
    }
}</style>

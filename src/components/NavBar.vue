<script setup>
import { ref } from 'vue'

const isOpen = ref(false)
</script>

<template>
    <nav class="bg-blue-600 text-white">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="flex justify-between items-center h-16">
                <!-- Logo -->
                <div class="flex-shrink-0">
                    <a href="#" class="text-2xl font-bold">Indeed</a>
                </div>

                <!-- Desktop Links -->
                <div class="hidden md:flex space-x-6">
                    <a href="#" class="hover:text-blue-200">Home</a>
                    <a href="#" class="hover:text-blue-200">Jobs</a>
                    <a href="#" class="hover:text-blue-200">Add Job</a>
                </div>

                <!-- Mobile Menu Button -->
                <div class="md:hidden">
                    <button @click="isOpen = !isOpen" class="focus:outline-none focus:ring-2 focus:ring-white rounded">
                        <svg class="h-6 w-6" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24"
                            stroke="currentColor">
                            <path v-if="!isOpen" stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                d="M4 6h16M4 12h16M4 18h16" />
                            <path v-else stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                d="M6 18L18 6M6 6l12 12" />
                        </svg>
                    </button>
                </div>
            </div>
        </div>

        <!-- Mobile Links -->
        <div v-if="isOpen" class="md:hidden px-2 pb-3 space-y-1">
            <a href="#" class="block px-3 py-2 rounded hover:bg-blue-700">Home</a>
            <a href="#" class="block px-3 py-2 rounded hover:bg-blue-700">About</a>
            <a href="#" class="block px-3 py-2 rounded hover:bg-blue-700">Contact</a>
        </div>
    </nav>
</template>

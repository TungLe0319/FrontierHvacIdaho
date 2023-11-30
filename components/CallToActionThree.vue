<script lang="ts" setup>
import Button from './Globals/Button.vue';
</script>

<template>
    <div class="relative py-16">
        <div aria-hidden="true"
            class="absolute inset-0 h-max w-full m-auto grid grid-cols-2 -space-x-52 opacity-40 dark:opacity-20">
            <div class="blur-[106px] h-72 bg-gradient-to-br from-teal-500 to-purple-400 dark:from-blue-700"></div>
            <div class="blur-[106px] h-52 bg-gradient-to-r from-cyan-400 to-sky-300 dark:to-indigo-600"></div>
        </div>
        <div class="max-w-7xl mx-auto px-6 md:px-12 xl:px-6">
            <div class="relative">
                <div class="flex items-center justify-center -space-x-2">
                    <img loading="lazy" width="400" height="400" src="https://randomuser.me/api/portraits/women/12.jpg"
                        alt="member photo" class="h-8 w-8 rounded-full object-cover">
                    <img loading="lazy" width="200" height="200" src="https://randomuser.me/api/portraits/women/45.jpg"
                        alt="member photo" class="h-12 w-12 rounded-full object-cover">
                    <img loading="lazy" width="200" height="200" src="https://randomuser.me/api/portraits/women/60.jpg"
                        alt="member photo" class="z-10 h-16 w-16 rounded-full object-cover">
                    <img loading="lazy" width="200" height="200" src="https://randomuser.me/api/portraits/women/4.jpg"
                        alt="member photo" class="relative h-12 w-12 rounded-full object-cover">
                    <img loading="lazy" width="200" height="200" src="https://randomuser.me/api/portraits/women/34.jpg"
                        alt="member photo" class="h-8 w-8 rounded-full object-cover">
                </div>
                <div class="mt-6 m-auto space-y-6 md:w-8/12 lg:w-7/12">
                    <h1 class="text-center text-6xl  font-bold text-gray-800 dark:text-white ">Get Started now
                    </h1>
                    <p class="text-center text-xl text-gray-600 dark:text-gray-300">
                        Be part of millions people around the world using tailus in modern User Interfaces.
                    </p>
                    <div class="flex flex-wrap justify-center gap-6">
                        <Button
                            class=" rounded-full  bg-[var(--auburn)]  text-white shadow-md  items-center justify-center  mb-4 text-2xl">
                            <span>Get Started </span>
                        </Button>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<style></style>

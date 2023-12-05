<template>
  <div class="p-10">
    <div class="relative max-w-7xl mx-auto shadow-xl ">
      <div class="max-w-lg mx-auto rounded-lg shadow-lg overflow-hidden lg:max-w-none lg:flex">
        <div
          class="flex-1 px-6 py-8 lg:p-12  transition-all duration-200 ">
          <h3 class="text-2xl font-extrabold  sm:text-3xl">Same Day Service</h3>
          <p class="mt-6  text-gray-500 sm:text-lg">Heading System install for as low as $89 + Free consultation &
            Same Day Service
          </p>
          <div class="mt-8">
            <div class="flex items-center">
              <div class="flex-1 border-t-2 border-gray-200"></div>
            </div>
            <ul role="list" class="mt-8 space-y-5 lg:space-y-0 lg:grid lg:grid-cols-2 lg:gap-x-8 lg:gap-y-5">
              <li class="flex items-start lg:col-span-1" v-for="i in items">
                <Icon :name="i.icon" class="text-green-400 text-3xl" />
                <p class="ml-3 ">{{ i.content }}</p>
              </li>
            </ul>
          </div>
        </div>
        <div
          class="py-8 px-6 text-center lg:flex-shrink-0 lg:flex lg:flex-col lg:justify-center lg:p-12 ">
          <p class="text-lg leading-6 font-medium ">Pay once, own it forever</p>
          <div class="mt-4 flex items-center justify-center text-5xl font-extrabold ">
            <span>$19.99</span><span class="ml-3 text-xl font-medium text-gray-50">USD</span>
          </div>
          <div class="mt-6">
            <Button class="bg-[var(--auburn)] rounded-full  hover:shadow-xl">
              Get started
            </Button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>
import Button from './Globals/Button.vue';
const items = [
  { content: 'Analyze your new heating system installation needs', icon: 'mdi:check-bold' },
  { content: 'NO service call fees.', icon: 'mdi:check-bold' },
  { content: 'NO service call fees.NO dispatch fees', icon: 'mdi:check-bold' },
  { content: 'Analyze your new heating system installation needs', icon: 'mdi:check-bold' },

]

// We will come to your home
// Analyze your new heating system installation needs
// Present you with personalized solutions on what to do next
// Financing Options Available!
// 100 % satisfaction guaranteed
// NO service call fees.NO dispatch fees
</script>

<style></style>
<template>
  <div class="relative overflow-hidden ">
    <div class="lg:absolute flex items-center justify-center right-0 top-0 z-10">
      <img src="/ac.png" alt="AC Unit Icon" class="w-4/5 shadow-none hover:brightness-100">
    </div>
    <div class="absolute  inset-x-0 bottom-20  lg:bottom-0  ">
      <svg height="660" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320">
        <path fill="#341e65" fill-opacity="1" d="M0,32L1440,96L1440,320L0,320Z"></path>
      </svg>
    </div>
    <div class="  flex items-center justify-startB lg:justify-start w-full  px-4 py-16  sm:max-w-xl md:max-w-full lg:max-w-screen-xl md:px-24 lg:px-8 lg:py-20">
      <div class=" w-1/2 text-center  relative  flex flex-col items-center ">
        <h2 class="mb-6  text-6xl text-center font-bold  text-white ">
          Ready to Schedule?
        </h2>
        <p class="mb-6 text-base text-indigo-200 md:text-lg">
          Ready to experience top-notch HVAC services? Schedule your service now to ensure a comfortable and efficient
          home environment. Our expert technicians are prepared to address your heating and cooling needs promptly.
          Don't wait—book your appointment for reliable and timely HVAC solutions.
        </p>
       <PhoneNumberBtn/>
        <p class="max-w-md my-5 text-xs tracking-wide text-indigo-100 sm:text-sm sm:mx-auto md:mb-16">
          Take the first step towards a perfectly climate-controlled home.
        </p>
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>

import PhoneNumberBtn from './Globals/PhoneNumberBtn.vue';
</script>

<style></style>
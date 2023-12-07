<template>
  <div class="hero-image relative">
    <div class=" absolute z-10 h-full w-full flex flex-col items-center justify-center text-7xl text-white font-bold shadow-xl space-y-5 ">
   <div class="">
       24-Hour Service Available! 
      
   </div>
   <div class="">
     (208)  921-232
   </div>
    </div>

    <div class="absolute w-full h-full bg-black/50 top-0"></div>
  </div>
</template>

<script lang="ts" setup>

</script>

<style>
.hero-image{
  height: 25vh;
  /* always scale the image to the appropriate size of your screen */
  background-size: cover;
  background-image: url('https://images.unsplash.com/photo-1545866166-a2cf173536da?q=80&w=2070&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D');
  background-position: center;
  /* keeps the image fixed while scrolling , neat effect. */
  background-attachment: fixed; 
}
</style>
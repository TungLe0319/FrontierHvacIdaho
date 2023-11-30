<script lang="ts" setup>
import IconList from './Globals/IconList.vue'
import Button from './Globals/Button.vue'

// import ButtonWithIcon from "../../../packages/Shared-Components/Buttons/ButtonWithIcon.vue";

const iconListItems = [
  { icon: 'mdi:check-bold', text: 'Reliable Performance:', iconColor: 'rgb(245 158 11)' },
  { icon: 'mdi:check-bold', text: 'Smart Energy Solutions', iconColor: 'rgb(245 158 11)' },
  { icon: 'mdi:check-bold', text: 'Optimized Climate Control', iconColor: 'rgb(245 158 11)' },
]
</script>

<template>
  <div class="  mt-32  min-h-screen flex items-center justify-center relative overflow-hidden">
    <div class="lg:flex justify-center items-center gap-2 w-full px-5  lg:px-10 ">
      <div class=" text-start lg:w-2/3 flex flex-col items-start justify-center space-y-5 mb-10 ">
        <h1 class="     text-white  text-5xl font-bold  lg:text-7xl     drop-shadow-md">
      Transforming Spaces with Smart Climate Solutions
        </h1>

       
        <h2 class=" font-bold  text-2xl ">
      Delivering cutting-edge HVAC solutions tailored for your comfort and efficiency needs. Our expertise ensures a seamless blend of technology and performance to redefine your living or working environment.
        </h2>
        <Button class=" rounded-full shadow-md flex items-center justify-center gap-2">
          <span>Experience Superior Comfort Today</span>
          <Icon name="material-symbols:arrow-right-alt" size="30" />
        </Button>
        <IconList :items="iconListItems" icon-size="28px">
          <template #item-0>
            <span class=" font-semibold text-xl"> {{ iconListItems[0].text }}</span>
          </template>
          <template #item-1>
            <span class=" font-semibold text-xl"> {{ iconListItems[1].text }}</span>
          </template>
          <template #item-2>
            <span class=" font-semibold text-xl"> {{ iconListItems[2].text }}</span>
          </template>
        </IconList>
        <div class="flex justify-center items-center gap-2" />
      </div>
      <div class="lg:w-1/2 items-center flex justify-center">
       <img src="/heating.png" alt="Heating free icon" class=" shadow-none hover:brightness-100 ">
      </div>
    </div>
    <div class=" absolute  -z-50    top-0  ">
   <svg width="100vw" height="100vh" id="svg" viewBox="10 900 1140 -40" xmlns="http://www.w3.org/2000/svg" class="transition duration-300 ease-in-out delay-150"><defs><linearGradient id="gradient" x1="0%" y1="50%" x2="100%" y2="50%"><stop offset="5%" stop-color="#0693e3"></stop><stop offset="95%" stop-color="#9900ef"></stop></linearGradient></defs><path d="M 0,600 C 0,600 0,120 0,120 C 66.0871794871795,129.4794871794872 132.174358974359,138.9589743589744 206,131 C 279.825641025641,123.04102564102563 361.3897435897435,97.64358974358973 455,97 C 548.6102564102565,96.35641025641027 654.2666666666668,120.4666666666667 733,136 C 811.7333333333332,151.5333333333333 863.5435897435898,158.48974358974357 941,158 C 1018.4564102564102,157.51025641025643 1121.5589743589744,149.57435897435897 1209,142 C 1296.4410256410256,134.42564102564103 1368.2205128205128,127.21282051282051 1440,120 C 1440,120 1440,600 1440,600 Z" stroke="none" stroke-width="0" fill="url(#gradient)" fill-opacity="0.265" class="transition-all duration-300 ease-in-out delay-150 path-0" transform="rotate(-180 720 300)"></path><defs><linearGradient id="gradient" x1="0%" y1="50%" x2="100%" y2="50%"><stop offset="5%" stop-color="#0693e3"></stop><stop offset="95%" stop-color="#9900ef"></stop></linearGradient></defs><path d="M 0,600 C 0,600 0,240 0,240 C 54.88205128205132,232.19230769230768 109.76410256410264,224.3846153846154 206,233 C 302.23589743589736,241.6153846153846 439.82564102564095,266.65384615384613 518,264 C 596.174358974359,261.34615384615387 614.9333333333334,231 691,224 C 767.0666666666666,217 900.4410256410256,233.34615384615384 984,230 C 1067.5589743589744,226.65384615384616 1101.302564102564,203.61538461538458 1169,202 C 1236.697435897436,200.38461538461542 1338.3487179487179,220.1923076923077 1440,240 C 1440,240 1440,600 1440,600 Z" stroke="none" stroke-width="0" fill="url(#gradient)" fill-opacity="0.4" class="transition-all duration-300 ease-in-out delay-150 path-1" transform="rotate(-180 720 300)"></path><defs><linearGradient id="gradient" x1="0%" y1="50%" x2="100%" y2="50%"><stop offset="5%" stop-color="#0693e3"></stop><stop offset="95%" stop-color="#9900ef"></stop></linearGradient></defs><path d="M 0,600 C 0,600 0,360 0,360 C 62.13589743589745,343.70000000000005 124.2717948717949,327.40000000000003 198,336 C 271.7282051282051,344.59999999999997 357.0487179487179,378.1 450,391 C 542.9512820512821,403.9 643.5333333333334,396.2 737,398 C 830.4666666666666,399.8 916.8179487179489,411.1 996,399 C 1075.1820512820511,386.9 1147.1948717948717,351.40000000000003 1220,341 C 1292.8051282051283,330.59999999999997 1366.4025641025642,345.29999999999995 1440,360 C 1440,360 1440,600 1440,600 Z" stroke="none" stroke-width="0" fill="url(#gradient)" fill-opacity="0.53" class="transition-all duration-300 ease-in-out delay-150 path-2" transform="rotate(-180 720 300)"></path><defs><linearGradient id="gradient" x1="0%" y1="50%" x2="100%" y2="50%"><stop offset="5%" stop-color="#0693e3"></stop><stop offset="95%" stop-color="#9900ef"></stop></linearGradient></defs><path d="M 0,600 C 0,600 0,480 0,480 C 80.3153846153846,503.1435897435897 160.6307692307692,526.2871794871794 230,518 C 299.3692307692308,509.71282051282054 357.79230769230776,469.99487179487176 454,468 C 550.2076923076922,466.00512820512824 684.1999999999999,501.7333333333333 761,496 C 837.8000000000001,490.2666666666667 857.4076923076923,443.07179487179496 928,447 C 998.5923076923077,450.92820512820504 1120.1692307692308,505.97948717948714 1214,520 C 1307.8307692307692,534.0205128205129 1373.9153846153845,507.01025641025643 1440,480 C 1440,480 1440,600 1440,600 Z" stroke="none" stroke-width="0" fill="url(#gradient)" fill-opacity="1" class="transition-all duration-300 ease-in-out delay-150 path-3" transform="rotate(-180 720 300)"></path></svg>

    </div>
  </div>
</template>

<style>
.hero-image {
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  /* always scale the image to the appropriate size of your screen */
  background-size: cover;
  background-image: url("https://images.unsplash.com/photo-1619472351888-f844a0b33f5b?q=80&w=2128&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D");
  background-position: center;
  /* keeps the image fixed while scrolling , neat effect. */
  background-attachment: fixed;
}
</style>

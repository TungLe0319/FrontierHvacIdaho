<template>
  <div class="flex flex-col justify-center items-center">
    <div class=" w-2/3">
      <SectionHeader header="Hvac" title="Brand we service" content="
" />
     
    </div>
     <div class="flex flex-wrap my-10  gap-6 items-center justify-center">
          <div v-for="item in items" :key="item.img" class="">
            <img :src="item.img" class="shadow-none object-cover   " alt="">
          </div>
        </div>
  </div>
</template>

<script lang="ts" setup>
const items = [
  {
    img: 'https://nrgair.com/wp-content/uploads/2022/09/goodman-logo-1-300x141.jpg',
  },
  {
    img: 'https://nrgair.com/wp-content/uploads/2022/09/Trane_logo.svg_-300x100.png',
  },
  {
    img: 'https://nrgair.com/wp-content/uploads/2022/09/Lennox_Logo_Colour_CMYK-300x94.png',
  }, {
    img: 'https://nrgair.com/wp-content/uploads/2022/09/carrier-vector-logo-300x167.png',
  },

  {
    img: 'https://nrgair.com/wp-content/uploads/2022/09/dayandnight-logo.png',
  },
  {
    img: 'https://nrgair.com/wp-content/uploads/2022/09/Daikin-Logo-1-300x169.jpg',
  },

]
</script>

<style></style>
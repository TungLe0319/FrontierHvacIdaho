<template>
  <div class="flex flex-col justify-center items-center ">
    <div class=" w-2/3">
      <SectionHeader header="Hvac" title="Brands we service" content="
" />
    </div>
    <div class="flex flex-wrap my-10  gap-10 items-center justify-center">
      <a :href="item.link" v-for="item in items" :key="item.img" target="_blank"
        class=" p-2 hover:shadow-xl rounded-md transition-all duration-300">
        <img :src="item.img" class="shadow-none object-cover  shadow-none hover:brightness-100  " :alt="item.title">
      </a>
    </div>
  </div>
</template>

<script lang="ts" setup>
const items = [
  {
    title: 'Goodman',
    img: 'https://nrgair.com/wp-content/uploads/2022/09/goodman-logo-1-300x141.jpg',
    link: 'https://www.goodmanmfg.com/'
  },
  {
    title: 'Trane',
    img: 'https://nrgair.com/wp-content/uploads/2022/09/Trane_logo.svg_-300x100.png',
    link: 'https://www.trane.com/index.html'
  },
  {
    title: 'Lennox',
    img: 'https://nrgair.com/wp-content/uploads/2022/09/Lennox_Logo_Colour_CMYK-300x94.png',
    link: 'https://www.lennox.com/'
  }, {
    title: 'Carrier',
    img: 'https://nrgair.com/wp-content/uploads/2022/09/carrier-vector-logo-300x167.png',
    link: 'https://www.carrier.com/carrier/en/worldwide/'
  },

  {
    title: 'York',
    img: 'https://nrgair.com/wp-content/uploads/2022/09/Screenshot-2022-08-29-084742-300x107.jpg',
    link: 'https://www.york.com/'
  },
  {
    title: 'Diakin',
    img: 'https://nrgair.com/wp-content/uploads/2022/09/Daikin-Logo-1-300x169.jpg',
    link: 'https://www.northamerica-daikin.com/'
  },

]
</script>

<style scoped></style>
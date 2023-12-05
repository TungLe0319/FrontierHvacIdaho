<template>
  <!-- <div class=" flex flex-col items-center justify-center  mb-24">
    <div class=" text-5xl text-center  font-bold my-10">
      Testimonials
    </div>
    <hr class="  w-1/6  h-2 border-orange-400">
  </div> -->
  <SectionHeaderCenter title="Testimonials" header="What our customers say"
    content="Lorem ipsum dolor sit amet, consectetur adipisicing elit. Quod eos id officiis hic tenetur quae quaerat ad velit ab hic." />
  <div class=" hero-image   mt-32 mb-20 flex items-center justify-center border-y-4 w-full border-orange-300  relative  text-center">
    <section class="  z-40 w-full p-10   flex  items-center justify-between  gap-2">
      <v-carousel hide-delimiter-background show-arrows="hover" progress="warning" cycle>
        <v-carousel-item v-for="item in items" :key="item" >
          <div class=" text-white  space-y-8 p-20 backdrop-blur-sm ">
            <v-rating hover readonly :length="5" size="x-large" half-increments :model-value="item.rating"
              color="grey darken-3" active-color="warning" />
            <div class="  font-bold text-5xl ">
              {{ item.title }}
            </div>
            <div class=" flex items-center justify-center space-x-5 ">
              <Icon name="bx:bxs-quote-alt-left" class="text-4xl text-white" />
              <span class="text-xl text-gray-300"> {{ item.content }}</span>
              <Icon name="bx:bxs-quote-alt-right" class="text-4xl text-white" />
            </div>
            <div class="font-bold text-2xl">
              - {{ item.name }}
            </div>
          </div>
        </v-carousel-item>
      </v-carousel>
    </section>
    <div
      class="absolute z-40 -top-9 left-1/2 -translate-x-1/2  rounded-full   shadow-xl shadow-black/50 border-8 border-black/30 hover:shadow-xl transition-all duration-150 ">
      <Icon name='logos:teamwork-icon' class="text-amber-400 text-6xl" />
    </div>
    <div class="bg-black/60 absolute w-full h-full"></div>
  </div>
</template>

<script lang="ts" setup>


const items = [
  {
    name: 'John Doe',
    title: 'Customers for life!',
    content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quod eos id officiis hic tenetur quae quaerat ad velit ab hic.',
    rating: 5
  },
  {
    name: 'Jane Doe',
    title: 'Customers for life!',
    content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quod eos id officiis hic tenetur quae quaerat ad velit ab hic.',
    rating: 4.5
  },
  {
    name: 'Jake ',
    title: 'Customers for life!',
    content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quod eos id officiis hic tenetur quae quaerat ad velit ab hic.',
    rating: 4
  },
  {
    name: 'Tom',
    title: 'Customers for life!',
    content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quod eos id officiis hic tenetur quae quaerat ad velit ab hic.',
    rating: 4.5
  },
  {
    name: 'Daniel',
    title: 'Customers for life!',
    content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quod eos id officiis hic tenetur quae quaerat ad velit ab hic.',
    rating: 4
  },
  {
    name: 'Jessica4',
    title: 'Customers for life!',
    content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quod eos id officiis hic tenetur quae quaerat ad velit ab hic.',
    rating: 5
  },
  {
    name: 'William',
    title: 'Customers for life!',
    content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quod eos id officiis hic tenetur quae quaerat ad velit ab hic.',
    rating: 5
  },
  {
    name: 'Jackie',
    title: 'Customers for life!',
    content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quod eos id officiis hic tenetur quae quaerat ad velit ab hic.',
    rating: 5
  },
  {
    name: 'Jeremy',
    title: 'Customers for life!',
    content: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Quod eos id officiis hic tenetur quae quaerat ad velit ab hic.',
    rating: 5
  }
]



</script>

<style scoped>
.hero-image {
  height: 75vh;
  /* always scale the image to the appropriate size of your screen */
  background-size: cover;
  background-image: url('https://images.unsplash.com/photo-1623005470778-6d6e27b75186?q=80&w=2070&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D');
  background-position: center;
  /* keeps the image fixed while scrolling , neat effect. */
  background-attachment: fixed;

}
</style>
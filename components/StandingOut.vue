<script setup lang="ts">
const benefits = [
  {
    title: 'Elevate Your Digital Presence',
    content: 'Transform your online presence with innovative and cutting-edge solutions.',
    image: 'https://images.unsplash.com/photo-1640087975859-f2e7a8d09634?q=80&w=2069&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D',
  },
  {
    title: 'Craft Seamless Solutions',
    content: 'Create user-friendly and efficient solutions for unmatched online success.',
    image: 'https://images.unsplash.com/photo-1465224414649-ceb7f1db3999?q=80&w=2070&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D',
  },

  {
    title: 'See the Transformation',
    content: 'Experience boosted engagement and a seamless digital transformation.',
    image: 'https://images.unsplash.com/photo-1511256094521-c1cf19529095?q=80&w=2069&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D',
  },

];
</script>

<template>
  <main class=" space-y-10 px-10 relative ">
    <SectionHeader title="Benefits of our Service" header="What we provide"
      content="Lorem ipsum dolor sit amet, consectetur adipisicing elit. Nostrum deserunt, porro quisquam rerum soluta laborum" />
    <section v-for="(benefit, index) in benefits" :key="benefit.title" v-motion-fade-visible
      class=" flex flex-col space-y-4  ">
      <div class="lg:flex  space-y-4 lg:space-y-0 ">
        <div :class="index % 2 === 0 ? ' order-1' : ' order-0'"
          class="flex   cool-img  lg:w-2/3 h-[300px]  lg:h-[700px] rounded-2xl xl:rounded-full shadow-xl"
          :style="{ backgroundImage: `url('${benefit.image}')` }">
        </div>
        <article :class="index % 2 === 1 ? ' order-1' : ' order-0'"
          class=" flex lg:w-1/2 flex-col space-y-6 items-center justify-center ">
          <h1 class="mb-0  text-4xl font-bold  ">
            {{ benefit.title }}
          </h1>
          <p>
            {{ benefit.content }}
          </p>
        </article>
      </div>
    </section>
  
  </main>
</template>

<style scoped>
.cool-img{
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  background-attachment: fixed;
}
</style>

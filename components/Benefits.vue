<script setup lang="ts">
const benefits = [
  {
      title: 'Year-Round Installation Expertise',
    content: 'Trust our skilled team for seamless installation of furnaces, air conditioners, ductless systems, and more.',
    icon: 'meteocons:clear-day-fill', // Replace with a general installation icon URL
    image: 'https://images.unsplash.com/photo-1640087975859-f2e7a8d09634?q=80&w=2069&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D',
  },
  {
     title: 'Efficient Cooling Solutions',
    content: 'Stay cool and relaxed with our advanced air conditioning systems designed for maximum efficiency and performance.',
    icon: 'meteocons:snowflake-fill', // Replace with appropriate air conditioner icon URL
    image: 'https://images.unsplash.com/photo-1465224414649-ceb7f1db3999?q=80&w=2070&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D',
  },

  {
    title: 'Enhance Comfort All Year',
    content: 'Upgrade your living spaces with top-notch HVAC solutions, ensuring optimal comfort throughout the seasons.',
    icon: 'meteocons:wind', // Replace with appropriate furnace icon URL
    image: 'https://images.unsplash.com/photo-1511256094521-c1cf19529095?q=80&w=2069&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D',
  },

];





</script>

<template>
  <main class=" space-y-10 px-10 relative ">
  <SectionHeaderCenter header="Our Benefits" title="Why Choose Us?" content="We are a team of passionate and dedicated professionals who are committed to delivering exceptional results. We are here to help you achieve your goals and elevate your online presence." />
    <section v-for="(benefit, index) in benefits" :key="benefit.title" 
      class=" flex flex-col space-y-4  ">
      <div class="lg:flex items-center justify-center  space-y-4 lg:space-y-0 lg:mt-10 mt-5 ">
        <div :class="index % 2 === 0 ? ' order-1' : ' order-0'"
          class="flex   rounded-full   p-2 bg-gradient-to-r from-indigo-500 via-purple-500 to-orange-500  items-center justify-center "
         >
         <img :src="benefit.image" alt="" class="object-cover rounded-full w-96 h-96">
        </div>
        <article :class="index % 2 === 1 ? ' order-1' : ' order-0'"
          class=" flex lg:w-1/2 flex-col space-y-6 items-center justify-center  lg:p-10 p-4 ">
          <Icon :name="benefit.icon" class="text-9xl" />
          <h1 class="mb-0  text-2xl lg:text-4xl font-bold  ">
            {{ benefit.title }}
          </h1>
          <p class="p-4  text-xl lg:text-xl ">
            {{ benefit.content }}
          </p>
        </article>
      </div>
    </section>
  </main>
</template>

<style scoped>
.cool-img {
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
  background-attachment: fixed;
  @media screen and (max-width: 768px) {
 
    background-attachment: scroll;
  }
}


@keyframes rotate {
  0% {
    transform: rotate(0deg);
  }
  100% {
    transform: rotate(360deg);
  }
}
.rotate {
  animation: rotate 20s linear infinite;
}
</style>

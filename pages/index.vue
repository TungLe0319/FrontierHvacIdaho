<script lang="ts" setup>
import Hero from '../components/Hero.vue'
import Reviews from '~/components/Reviews.vue';
</script>

<template>
  <div class="flex flex-col space-y-10 lg:space-y-20  lg:mt-0  ">
    <Hero />
    <ProblemSolution />
    <div id="features">
      <Features />
    </div>
    <CallToActionTwo />
    <div id="benefits">
      <Benefits />
    </div>
    <div id="about">
      <About />
    </div>
    <div id="pricing">
      <PricingPlan />
    </div>
    <div id="reviews">
      <Reviews />
    </div>
    <div id="faq">
      <FAQ />
    </div>
    <div id="contact">
      <CallToActionThree />
    </div>
    <ContactForm />
  </div>
</template>

<style></style>

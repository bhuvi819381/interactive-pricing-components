<script setup lang="ts">
import Card from './components/Card.vue';
</script>

<template>
  <main
    class="mx-auto h-screen w-full max-w-[90rem] bg-[url('/images/bg-pattern.svg')] bg-no-repeat"
  >
    <div
      class="item-center relative place-items-center w-full pt-[4rem] text-center"
    >
      <img src="/images/pattern-circles.svg" alt="" class="absolute left-1/2 -translate-x-1/2" />
      <h1 class="mt-[2.5rem] font-bold text-[1.78rem] text-CTA-bg">Simple, traffic-based pricing</h1>
      <p class="text-[0.938rem] mt-[0.4rem]">Sign-up for our 30-day trial. No credit card required.</p>
    </div>
    <div class="flex justify-center  items-center w-full ">
      <Card />
    </div>
  </main>
</template>

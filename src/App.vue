<script setup lang="ts">
import Card from "./components/Card.vue";
</script>

<template>
  <main
    class="mx-auto h-screen w-full max-w-[90rem] bg-[url('/images/bg-pattern.svg')] bg-no-repeat"
  >
    <div
      class="item-center relative w-full place-items-center pt-[4rem] text-center"
    >
      <img
        src="/images/pattern-circles.svg"
        alt=""
        class="absolute left-1/2 -translate-x-1/2"
      />
      <h1 class="text-CTA-bg mt-[2.5rem] text-[1.78rem] font-bold">
        Simple, traffic-based pricing
      </h1>
      <p class="mt-[0.4rem] text-[0.938rem]">
        Sign-up for our 30-day trial. No credit card required.
      </p>
    </div>
    <div class="flex w-full items-center justify-center">
      <Card />
    </div>
  </main>
</template>

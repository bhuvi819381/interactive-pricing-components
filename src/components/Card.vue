<script setup lang="ts">
import { computed, ref } from "vue";

const value = ref(50);

const sliderFill = computed(() => {
  const percent = ((value.value - 1) / 99) * 100;
  return `--percent: ${percent}%`;
});
</script>

<template>
  <div
    class="bg-main-bg mt-[5.6rem] w-[33.7rem] rounded-md px-[2.8rem] shadow-lg"
  >
    <div class="mt-[2.5rem] flex items-center justify-between">
      <h2 class="text-[0.938rem] tracking-[0.1186rem] uppercase">
        100K Pageviews
      </h2>
      <p class="text-center">
        <span class="text-CTA-bg text-[2.5rem] font-bold">$16.00 </span> / month
      </p>
    </div>

    <div class="mt-[1.7rem]">
      <input
        type="range"
        name=""
        id=""
        min="1"
        max="100"
        v-model="value"
        class="custom-slider bg-empty-slidebar h-[0.6rem] w-full appearance-none rounded-xl transition-opacity outline-none"
        :style="sliderFill"
      />
    </div>

    <div class="mt-[3rem] flex items-center justify-center space-x-3 text-sm">
      <span class="text-xs">Monthly Billing</span>

      <label class="relative inline-flex cursor-pointer items-center">
        <input type="checkbox" class="peer sr-only" />
        <div
          class="peer bg-toggle-bg peer-checked:bg-slider-bg h-5 w-10 rounded-full peer-focus:outline-none after:absolute after:top-[2px] after:left-[3px] after:h-4 after:w-4 after:rounded-full after:border after:border-gray-300 after:bg-white after:transition-all peer-checked:after:translate-x-full peer-checked:after:border-white"
        ></div>
      </label>

      <span class="flex items-center gap-1 text-xs">
        Yearly Billing
        <span
          class="bg-discount-bg text-discount-text rounded-full px-2 py-0.5 text-xs font-bold"
          >25% discount</span
        >
      </span>
    </div>

    <hr class="mt-[2.3rem]" />

    <div class="my-[2rem] flex items-center justify-between">
      <ul>
        <li class="text-[0.7rem]">Unlimited websites</li>
        <li class="my-3 text-[0.7rem]">100% data ownership</li>
        <li class="text-[0.7rem]">Email reports</li>
      </ul>
      <button
        class="bg-CTA-bg text-CTA-text cursor-pointer rounded-full px-12 py-3 text-xs"
      >
        Start my trial
      </button>
    </div>
  </div>
</template>

<style scoped>
.custom-slider::-webkit-slider-thumb {
  appearance: none;
  width: 2.5rem;
  height: 2.5rem;
  border-radius: 50%;
  background-color: var(--color-slider-bg);
  background-image: url("/images/icon-slider.svg");
  background-position: center;
  background-repeat: no-repeat;
  cursor: pointer;
}

li::before {
  content: "";
  display: inline-block;
  margin-right: 0.5rem;
  background: url("/images/icon-check.svg");
  background-size: contain;
  background-repeat: no-repeat;
  width: 0.6rem;
  height: 0.6rem;
}

/* .custom-slider::-webkit-slider-runnable-track {
  height: 8px;
  border-radius: 50%;
  background: linear-gradient(
    to right,
    #2dd4bf 0%,
    #2dd4bf calc(var(--percent) * 1%),
    #d1fae5 calc(var(--percent) * 1%),
    #d1fae5 100%
  );
  background-size: 100% 100%;
} */
</style>

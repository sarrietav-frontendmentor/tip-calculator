<template>
  <div
    class="
      bg-darkest-cyan
      p-6
      lg:p-10
      pt-10
      lg:pt-14
      rounded-xl
      flex flex-col
      lg:grow
      gap-6
    "
  >
    <BalanceSection label="Tip Amount" :amount="tipAmount" class="lg:mb-5" />
    <BalanceSection label="Total" :amount="totalAmount" class="lg:mb-auto" />
    <TheResetButton />
  </div>
</template>

<script lang="ts" setup>
import useStore from '@/store/mainStore';
import { computed } from 'vue';
import BalanceSection from './BalanceSection.vue';
import TheResetButton from './TheResetButton.vue';

const store = useStore();

const tipAmount = computed(() => store.tipAmount);
const totalAmount = computed(() => store.totalAmount);
</script>

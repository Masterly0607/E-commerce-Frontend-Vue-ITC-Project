<template>
  <div class="flex flex-col space-y-12 ml-36">
    <div class="flex space-x-6 items-center">
      <img src="@/assets/admin_assets/dashboard.png" alt="Dashboard" class="w-[36px]" />
      <p class="text-[32px] font-bold">Admin Dashboard</p>
    </div>
    <div class="flex space-x-8">
      <TotalCard title="Total Sales" total-number="$52,300" />
      <TotalCard title="Total Sales" total-number="214" />
      <TotalCard title="Total Revenues" total-number="$52,300" />
    </div>
  </div>
</template>
<script setup>
import TotalCard from '@/components/admin/TotalCard.vue'
</script>

<template>
  <div class="flex flex-col ml-36">
    <div class="flex flex-col space-y-8">
      <div class="flex space-x-6 items-center ml-12">
        <img src="@/assets/admin_assets/order.png" alt="Orders" class="w-[36px]" />
        <p class="text-[32px] font-bold">Manage Order</p>
      </div>
      <div class="flex space-x-6 text-[21px]">
        <button
          v-for="status in statuses"
          :key="status"
          @click="selectedStatus = status"
          :class="[
            'rounded-[5px] px-4 py-1 transition-colors duration-200 cursor-pointer',
            selectedStatus === status
              ? 'bg-[#ffc107] text-white'
              : 'bg-[#cad5e3] text-black hover:bg-[#b4c0d0]',
          ]"
        >
          {{ status }}
        </button>
      </div>
    </div>
    <div class="flex justify-center w-full mt-14">
      <table class="table-auto border-collapse border border-gray-300 w-full text-center mr-3">
        <thead>
          <tr class="bg-[#CAD5E3] text-[24px] w-full">
            <th class="px-4 py-2 border">Order ID</th>
            <th class="px-4 py-2 border">Customer</th>
            <th class="px-4 py-2 border">Total ($)</th>
            <th class="px-4 py-2 border">Status</th>
            <th class="px-4 py-2 border">Date</th>
            <th class="px-4 py-2 border">Action</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td class="px-4 py-2 border font-semibold">#101</td>
            <td class="px-4 py-2 border font-semibold">John Doe</td>
            <td class="px-4 py-2 border font-semibold">$146.99</td>
            <td class="px-4 py-2 border">
              <p class="bg-[#FCFE9C] text-[#EFBC22] rounded-[5px]">Processing</p>
            </td>
            <td class="px-4 py-2 border">2025-03-01</td>
            <td class="px-4 py-2 border">
              <div class="flex justify-center space-x-2">
                <p class="bg-[#2563EB] text-white cursor-pointer px-1 rounded-[3px]">Ship</p>
                <p class="bg-[#FF0000] text-white cursor-pointer px-1 rounded-[3px]">Cancel</p>
              </div>
            </td>
          </tr>
          <tr>
            <td class="px-4 py-2 border font-semibold">#103</td>
            <td class="px-4 py-2 border font-semibold">Jane Smith</td>
            <td class="px-4 py-2 border font-semibold">$146.99</td>
            <td class="px-4 py-2 border">
              <p class="bg-[#749be5] text-[#0000ff] rounded-[5px]">Shipped</p>
            </td>
            <td class="px-4 py-2 border">2025-03-01</td>
            <td class="px-4 py-2 border">
              <div class="flex justify-center space-x-2">
                <p class="bg-[#1ed937] text-white cursor-pointer px-1 rounded-[3px]">Deliver</p>
              </div>
            </td>
          </tr>
          <tr>
            <td class="px-4 py-2 border font-semibold">#105</td>
            <td class="px-4 py-2 border font-semibold">Alice Brown</td>
            <td class="px-4 py-2 border font-semibold">$146.99</td>
            <td class="px-4 py-2 border">
              <p class="bg-[#9cf9ab] text-[#158f46] rounded-[5px]">Delivered</p>
            </td>
            <td class="px-4 py-2 border">2025-03-01</td>
            <td class="px-4 py-2 border"></td>
          </tr>
          <tr>
            <td class="px-4 py-2 border font-semibold">#107</td>
            <td class="px-4 py-2 border font-semibold">Mark Johnson</td>
            <td class="px-4 py-2 border font-semibold">$146.99</td>
            <td class="px-4 py-2 border">
              <p class="bg-[#faaeae] text-[#ff0000] rounded-[5px]">Canceled</p>
            </td>
            <td class="px-4 py-2 border">2025-03-01</td>
            <td class="px-4 py-2 border"></td>
          </tr>
          <tr>
            <td class="px-4 py-2 border font-semibold">#109</td>
            <td class="px-4 py-2 border font-semibold">Sophia Lee</td>
            <td class="px-4 py-2 border font-semibold">$146.99</td>
            <td class="px-4 py-2 border">
              <p class="bg-[#FCFE9C] text-[#EFBC22] rounded-[5px]">Processing</p>
            </td>
            <td class="px-4 py-2 border">2025-03-01</td>
            <td class="px-4 py-2 border">
              <div class="flex justify-center space-x-2">
                <p class="bg-[#2563EB] text-white cursor-pointer px-1 rounded-[3px]">Ship</p>
                <p class="bg-[#FF0000] text-white cursor-pointer px-1 rounded-[3px]">Cancel</p>
              </div>
            </td>
          </tr>
        </tbody>
      </table>
    </div>
    <div class="flex justify-center mt-5 space-x-3 items-center">
      <div class="flex space-x-2 border px-5 py-2 rounded-[3px] bg-[#CAD5E3] cursor-pointer">
        <img
          src="@/assets/admin_assets/arrow_left.png"
          alt="Arrow Left"
          class="w-[22px] h-[22px]"
        />
        <p>Prev</p>
      </div>
      <p class="text-[21px]">1 of 2</p>
      <div class="flex space-x-2 border px-5 py-2 rounded-[3px] bg-[#CAD5E3] cursor-pointer">
        <p>Next</p>
        <img
          src="@/assets/admin_assets/arrow_right.png"
          alt="Arrow Right"
          class="w-[22px] h-[22px]"
        />
      </div>
    </div>
  </div>
</template>
<script setup>
import { ref } from 'vue'

const selectedStatus = ref('All')

const statuses = ['All', 'Processing', 'Shipped', 'Delivered', 'Canceled']
</script>

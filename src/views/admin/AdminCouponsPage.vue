<template>
  <div class="flex flex-col ml-36">
    <div class="flex flex-col space-y-8">
      <div class="flex space-x-6 items-center ml-12">
        <img src="@/assets/admin_assets/coupon.png" alt="Coupons" class="w-[36px]" />
        <p class="text-[32px] font-bold">Manage Coupons</p>
      </div>
      <form class="flex text-[21px] px-10 py-6 border rounded-[3px] flex-col space-y-10 mr-3">
        <div class="flex items-center space-x-2">
          <img src="@/assets/admin_assets/plus.png" alt="Plus Icon" class="w-[18px] h-[18px]" />
          <p>Add new Coupons</p>
        </div>
        <div class="flex justify-between w-full space-x-16">
          <div class="flex flex-col space-y-2 w-1/3">
            <label for="coupon_code" class="ml-4">Coupon Code</label>
            <input
              type="text"
              id="coupon_code"
              placeholder="Enter coupon code"
              class="border lg:pl-4 py-4 rounded-[5px] placeholder:text-gray-400"
            />
          </div>
          <div class="flex flex-col space-y-2 w-1/3">
            <label for="coupon_percent" class="ml-4">Discount (%)</label>
            <input
              type="text"
              id="coupon_percent"
              placeholder="Enter discount"
              class="border lg:pl-4 py-4 rounded-[5px] placeholder:text-gray-400"
            />
          </div>
          <div class="flex flex-col space-y-2 w-1/3">
            <label for="expiry_date" class="ml-4">Expiry Date</label>
            <input
              type="date"
              id="expiry_date"
              placeholder="Enter discount"
              class="border lg:px-4 py-4 rounded-[5px] text-gray-400"
            />
          </div>
        </div>
        <button
          type="submit"
          class="bg-[#FFC107] text-white px-10 py-1 rounded-[5px] w-fit cursor-pointer"
        >
          Save
        </button>
      </form>
    </div>
    <div class="flex flex-col space-y-5 w-full mt-14">
      <p class="text-[#158f46] text-4xl">Active Coupons</p>
      <table class="table-auto border-collapse border border-gray-300 text-center mr-3">
        <thead>
          <tr class="bg-[#CAD5E3] w-full">
            <th class="px-4 py-2 border">Code</th>
            <th class="px-4 py-2 border">Discount (%)</th>
            <th class="px-4 py-2 border">Expires On</th>
            <th class="px-4 py-2 border">Action</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td class="px-4 py-2 border">#103</td>
            <td class="px-4 py-2 border">20%</td>
            <td class="px-4 py-2 border text-[#FF0000]">2025-03-01</td>
            <td class="px-4 py-2 border">
              <div class="flex justify-center space-x-2">
                <p class="bg-[#2563EB] text-white cursor-pointer px-1 rounded-[3px]">Edit</p>
                <p class="bg-[#FF0000] text-white cursor-pointer px-1 rounded-[3px]">Delete</p>
              </div>
            </td>
          </tr>
          <tr>
            <td class="px-4 py-2 border">#105</td>
            <td class="px-4 py-2 border">20%</td>
            <td class="px-4 py-2 border">2025-04-04</td>
            <td class="px-4 py-2 border">
              <div class="flex justify-center space-x-2">
                <p class="bg-[#2563EB] text-white cursor-pointer px-1 rounded-[3px]">Edit</p>
                <p class="bg-[#FF0000] text-white cursor-pointer px-1 rounded-[3px]">Delete</p>
              </div>
            </td>
          </tr>
          <tr>
            <td class="px-4 py-2 border">#107</td>
            <td class="px-4 py-2 border">20%</td>
            <td class="px-4 py-2 border">2025-04-04</td>
            <td class="px-4 py-2 border">
              <div class="flex justify-center space-x-2">
                <p class="bg-[#2563EB] text-white cursor-pointer px-1 rounded-[3px]">Edit</p>
                <p class="bg-[#FF0000] text-white cursor-pointer px-1 rounded-[3px]">Delete</p>
              </div>
            </td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>
<script setup></script>

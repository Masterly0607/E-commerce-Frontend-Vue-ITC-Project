<template>
  <div class="flex flex-col ml-36 space-y-10">
    <div class="flex flex-col space-y-8">
      <div class="flex space-x-6 items-center ml-12">
        <img src="@/assets/admin_assets/messages.png" alt="Messages" class="w-[36px]" />
        <p class="text-[32px] font-bold">Contact Messages</p>
      </div>
      <div class="flex justify-center w-full mt-5">
        <table class="table-auto border-collapse border border-gray-300 w-full text-center mr-3">
          <thead>
            <tr class="bg-[#CAD5E3] text-[24px] w-full">
              <th class="px-4 py-2 border">Name</th>
              <th class="px-4 py-2 border">Email</th>
              <th class="px-4 py-2 border">Message</th>
              <th class="px-4 py-2 border">Reply</th>
            </tr>
          </thead>
          <tbody>
            <tr>
              <td class="px-4 py-2 border">John Doe</td>
              <td class="px-4 py-2 border">johndoe@example.com</td>
              <td class="px-4 py-2 border">I need help with my order.</td>
              <td class="px-4 py-2 border">
                <div class="flex justify-center space-x-2">
                  <p class="bg-[#2563EB] text-white cursor-pointer px-1 rounded-[3px]">Reply</p>
                </div>
              </td>
            </tr>
            <tr>
              <td class="px-4 py-2 border">Alice Brown</td>
              <td class="px-4 py-2 border">alice@example.com</td>
              <td class="px-4 py-2 border">Can I return my product?</td>
              <td class="px-4 py-2 border text-[#34c04d]" v-if="!haveReplied">
                Yes, you can return it within 30 days
              </td>
              <td class="px-4 py-2 border" v-else>
                <div class="flex justify-center space-x-2">
                  <p class="bg-[#2563EB] text-white cursor-pointer px-1 rounded-[3px]">Reply</p>
                </div>
              </td>
            </tr>
            <tr>
              <td class="px-4 py-2 border">Mark Smith</td>
              <td class="px-4 py-2 border">mark@example.com</td>
              <td class="px-4 py-2 border">Do you ship internationally?</td>
              <td class="px-4 py-2 border">
                <div class="flex justify-center space-x-2">
                  <p class="bg-[#2563EB] text-white cursor-pointer px-1 rounded-[3px]">Reply</p>
                </div>
              </td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>
  </div>
</template>
<script setup>
import { ref } from 'vue'

const haveReplied = ref(false)
</script>

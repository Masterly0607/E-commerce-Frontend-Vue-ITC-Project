<template>
  <div class="flex flex-col">
    <div class="flex flex-col space-y-8">
      <div class="flex space-x-6 items-center ml-12">
        <img src="@/assets/admin_assets/user.png" alt="User" class="w-[36px]" />
        <p class="text-[32px] font-bold">Manage User</p>
      </div>
      <div class="flex justify-between items-center">
        <div class="flex space-y-4 flex-col">
          <div class="flex items-center relative">
            <img
              src="@/assets/admin_assets/search.png"
              alt="Search"
              class="w-[30px] h-[30px] absolute left-3 pointer-events-none"
            />
            <input
              type="text"
              placeholder="Search Users..."
              class="w-[600px] h-[41px] border-black border-[1px] rounded-md pl-16 placeholder:text-[#877E7E] placeholder:text-[16px] font-light"
            />
          </div>
          <button
            class="rounded-[3px] bg-[#FFC107] w-[123px] h-[36px] text-white text-[16px] font-bold"
          >
            + Add User
          </button>
        </div>
        <div class="flex border-black border-[1px] h-fit px-2 rounded-[3px] mr-4 cursor-pointer">
          <p class="text-[21px] font-light">All Role</p>
          <img
            src="@/assets/admin_assets/chevron_down.png"
            alt="Chevron Down"
            class="w-[32px] h-[32px] ml-1"
          />
        </div>
      </div>
    </div>
    <div class="flex justify-center w-full mt-5">
      <table class="table-auto border-collapse border border-gray-300 w-full text-center mr-3">
        <thead>
          <tr class="bg-[#CAD5E3] text-[24px] w-full">
            <th class="px-4 py-2 border">No.</th>
            <th class="px-4 py-2 border">Name</th>
            <th class="px-4 py-2 border">Email</th>
            <th class="px-4 py-2 border">Role</th>
            <th class="px-4 py-2 border">Action</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td class="px-4 py-2 border">1</td>
            <td class="px-4 py-2 border">Admin User</td>
            <td class="px-4 py-2 border">admin@gmail.com</td>
            <td class="px-4 py-2 border">Admin</td>
            <td class="px-4 py-2 border">
              <div class="flex justify-center space-x-2">
                <p class="bg-[#2563EB] text-white cursor-pointer px-1 rounded-[3px]">Edit</p>
                <p class="bg-[#FF0000] text-white cursor-pointer px-1 rounded-[3px]">Delete</p>
              </div>
            </td>
          </tr>
          <tr>
            <td class="px-4 py-2 border">2</td>
            <td class="px-4 py-2 border">Seller User</td>
            <td class="px-4 py-2 border">seller@gmail.com</td>
            <td class="px-4 py-2 border">Seller</td>
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

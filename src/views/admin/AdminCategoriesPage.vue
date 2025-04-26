<template>
  <div class="flex flex-col ml-36">
    <div class="flex flex-col space-y-8">
      <div class="flex space-x-6 items-center ml-12">
        <img src="@/assets/admin_assets/categories.png" alt="Products" class="w-[36px]" />
        <p class="text-[32px] font-bold">Manage Categories</p>
      </div>
      <div class="flex justify-between items-center">
        <div class="flex space-y-4 flex-col w-full mr-3">
          <div class="flex items-center relative">
            <img
              src="@/assets/admin_assets/search.png"
              alt="Search"
              class="w-[30px] h-[30px] absolute left-3 pointer-events-none"
            />
            <input
              type="text"
              placeholder="Search Categories..."
              class="w-full h-[41px] border-black border-[1px] rounded-md pl-16 placeholder:text-[#877E7E] placeholder:text-[16px] font-light"
            />
          </div>
          <button
            class="rounded-[3px] bg-[#FFC107] w-fit h-[36px] text-white text-[16px] font-bold p-2"
          >
            + Add Category
          </button>
        </div>
      </div>
    </div>
    <div class="flex justify-center w-full mt-5">
      <table
        class="table-auto border-collapse border border-gray-300 w-full text-center mr-3 h-[350px]"
      >
        <thead class="h-[100px]">
          <tr class="bg-[#CAD5E3] text-[24px] w-full">
            <th class="px-4 py-2 border">Icon</th>
            <th class="px-4 py-2 border">Category</th>
            <th class="px-4 py-2 border">Actions</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td class="px-4 py-2 border">📱</td>
            <td class="px-4 py-2 border">Electronics</td>
            <td class="px-4 py-2 border">
              <div class="flex justify-center space-x-2">
                <p class="bg-[#2563EB] text-white cursor-pointer px-1 rounded-[3px]">Edit</p>
                <p class="bg-[#FF0000] text-white cursor-pointer px-1 rounded-[3px]">Delete</p>
              </div>
            </td>
          </tr>
          <tr>
            <td class="px-4 py-2 border">👗</td>
            <td class="px-4 py-2 border">Fashion</td>
            <td class="px-4 py-2 border">
              <div class="flex justify-center space-x-2">
                <p class="bg-[#2563EB] text-white cursor-pointer px-1 rounded-[3px]">Edit</p>
                <p class="bg-[#FF0000] text-white cursor-pointer px-1 rounded-[3px]">Delete</p>
              </div>
            </td>
          </tr>
          <tr>
            <td class="px-4 py-2 border">🏡</td>
            <td class="px-4 py-2 border">Home & Kitchen</td>
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

<template>
  <div class="flex flex-col">
    <div class="flex flex-col space-y-8">
      <div class="flex space-x-6 items-center ml-12">
        <img src="@/assets/admin_assets/products.png" alt="Products" class="w-[36px]" />
        <p class="text-[32px] font-bold">Manage Products</p>
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
              placeholder="Search Products..."
              class="w-full h-[41px] border-black border-[1px] rounded-md pl-16 placeholder:text-[#877E7E] placeholder:text-[16px] font-light"
            />
          </div>
          <button
            class="rounded-[3px] bg-[#FFC107] w-fit h-[36px] text-white text-[16px] font-bold p-2"
          >
            + Add Products
          </button>
        </div>
      </div>
    </div>
    <div class="flex justify-center w-full mt-5">
      <table class="table-auto border-collapse border border-gray-300 w-full text-center mr-3">
        <thead>
          <tr class="bg-[#CAD5E3] text-[24px] w-full">
            <th class="px-4 py-2 border">Image</th>
            <th class="px-4 py-2 border">Product</th>
            <th class="px-4 py-2 border">Price</th>
            <th class="px-4 py-2 border">Stock</th>
            <th class="px-4 py-2 border">Action</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td class="px-4 py-2 border"></td>
            <td class="px-4 py-2 border">Laptop</td>
            <td class="px-4 py-2 border">$1239.00</td>
            <td class="px-4 py-2 border">10</td>
            <td class="px-4 py-2 border">
              <div class="flex justify-center space-x-2">
                <p class="bg-[#2563EB] text-white cursor-pointer px-1 rounded-[3px]">Edit</p>
                <p class="bg-[#FF0000] text-white cursor-pointer px-1 rounded-[3px]">Delete</p>
              </div>
            </td>
          </tr>
          <tr>
            <td class="px-4 py-2 border"></td>
            <td class="px-4 py-2 border">Laptop</td>
            <td class="px-4 py-2 border">$1239.00</td>
            <td class="px-4 py-2 border">10</td>
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

<template>
  <div class="flex flex-col space-y-8 ml-36">
    <div class="flex space-x-6 items-center ml-12">
      <img src="@/assets/admin_assets/user.png" alt="User" class="w-[36px]" />
      <p class="text-[32px] font-bold">Manage User</p>
    </div>
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
    <button class="rounded-[3px] bg-[#FFC107] w-[123px] h-[36px] text-white text-[16px] font-bold">
      + Add User
    </button>
  </div>
</template>

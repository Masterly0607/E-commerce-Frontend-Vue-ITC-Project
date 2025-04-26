<template>
  <div class="flex flex-col ml-36 space-y-10">
    <div class="flex flex-col space-y-8">
      <div class="flex space-x-6 items-center ml-12">
        <img src="@/assets/admin_assets/settings.png" alt="Settings" class="w-[36px]" />
        <p class="text-[32px] font-bold">Admin Settings</p>
      </div>
      <form class="flex text-[21px] px-10 py-6 border rounded-[3px] flex-col space-y-10 mr-3">
        <p class="text-[#294a9d] text-[28px]">SEO Settings</p>
        <div class="flex flex-col space-y-5">
          <div class="flex flex-col space-y-2">
            <label for="site_title" class="ml-4 text-[#3b709c]">Site Title</label>
            <input
              type="text"
              id="site_title"
              placeholder="Enter site title"
              value="MyStore - Best E-Commerce"
              class="border lg:pl-4 py-4 rounded-[5px] placeholder:text-gray-400"
            />
          </div>
          <div class="flex flex-col space-y-2">
            <label for="meta_description" class="ml-4 text-[#3b709c]">Meta Description</label>
            <textarea
              rows="5"
              id="meta_description"
              placeholder="Enter meta description"
              class="border lg:pl-4 py-4 rounded-[5px] placeholder:text-gray-400"
            >
Buy high-quality product at unbeatable prices!
            </textarea>
          </div>
        </div>
        <button
          type="submit"
          class="bg-[#FFC107] text-white px-10 py-2 rounded-[5px] w-fit cursor-pointer"
        >
          Save Settings
        </button>
      </form>
    </div>
    <div class="w-full">
      <form class="flex text-[21px] px-10 py-6 border rounded-[3px] flex-col space-y-10 mr-3">
        <p class="text-[#294a9d] text-[28px]">API Security</p>
        <div class="flex space-x-5 items-center w-full justify-between">
          <label for="api_key" class="ml-4 text-[#3b709c] w-fit">API Key: </label>
          <input
            type="password"
            id="api_key"
            placeholder="Enter api key"
            readonly
            value="123456789abcdefg"
            class="border lg:pl-4 py-4 rounded-[5px] placeholder:text-gray-400 flex-1"
          />
        </div>
        <button
          type="submit"
          class="bg-[#D50F12] text-white px-10 py-2 rounded-[5px] w-fit cursor-pointer border-black border"
        >
          Reset API Key
        </button>
      </form>
    </div>
  </div>
</template>
<script setup></script>

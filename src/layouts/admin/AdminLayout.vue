<template>
  <div class="flex w-full min-h-screen">
    <div class="flex flex-col space-y-6 w-[250px] bg-gray-100 min-h-screen p-4">
      <p class="text-[32px] font-bold">Admin Panel</p>
      <RouterLink
        class="flex space-x-5 items-center"
        to="/admin"
        :class="$route.path === '/admin' ? 'bg-gray-200 rounded-[5px] py-1 pl-1' : ''"
      >
        <img src="@/assets/admin_assets/dashboard.png" alt="Dashboard" class="w-[36px] h-[36px]" />
        <p>Dashboard</p>
      </RouterLink>
      <RouterLink
        class="flex space-x-5 items-center"
        to="/admin/users"
        :class="$route.path === '/admin/users' ? 'bg-gray-200 rounded-[5px] py-1 pl-1' : ''"
      >
        <img src="@/assets/admin_assets/user.png" alt="Users" class="w-[36px] h-[36px]" />
        <p>Users</p>
      </RouterLink>
      <RouterLink
        class="flex space-x-5 items-center"
        to="/admin/products"
        :class="$route.path === '/admin/products' ? 'bg-gray-200 rounded-[5px] py-1 pl-1' : ''"
      >
        <img src="@/assets/admin_assets/products.png" alt="Products" class="w-[36px] h-[36px]" />
        <p>Products</p>
      </RouterLink>
      <RouterLink
        class="flex space-x-5 items-center"
        to="/admin/categories"
        :class="$route.path === '/admin/categories' ? 'bg-gray-200 rounded-[5px] py-1 pl-1' : ''"
      >
        <img
          src="@/assets/admin_assets/categories.png"
          alt="Categories"
          class="w-[36px] h-[36px]"
        />
        <p>Categories</p>
      </RouterLink>
      <RouterLink
        class="flex space-x-5 items-center"
        to="/admin/orders"
        :class="$route.path === '/admin/orders' ? 'bg-gray-200 rounded-[5px] py-1 pl-1' : ''"
      >
        <img src="@/assets/admin_assets/order.png" alt="Orders" class="w-[36px] h-[36px]" />
        <p>Orders</p>
      </RouterLink>
      <RouterLink
        class="flex space-x-5 items-center"
        to="/admin/coupons"
        :class="$route.path === '/admin/coupons' ? 'bg-gray-200 rounded-[5px] py-1 pl-1' : ''"
      >
        <img src="@/assets/admin_assets/coupon.png" alt="Coupons" class="w-[36px] h-[36px]" />
        <p>Coupons</p>
      </RouterLink>
      <RouterLink
        class="flex space-x-5 items-center"
        to="/admin/settings"
        :class="$route.path === '/admin/settings' ? 'bg-gray-200 rounded-[5px] py-1 pl-1' : ''"
      >
        <img src="@/assets/admin_assets/settings2.png" alt="Settings" class="w-[36px] h-[36px]" />
        <p>Settings</p>
      </RouterLink>
      <RouterLink
        class="flex space-x-5 items-center"
        to="/admin/messages"
        :class="$route.path === '/admin/messages' ? 'bg-gray-200 rounded-[5px] py-1 pl-1' : ''"
      >
        <img src="@/assets/admin_assets/messages.png" alt="Messages" class="w-[36px] h-[36px]" />
        <p>Contact Message</p>
      </RouterLink>
    </div>
    <div class="flex-1 p-6">
      <RouterView></RouterView>
    </div>
  </div>
</template>

<script setup></script>

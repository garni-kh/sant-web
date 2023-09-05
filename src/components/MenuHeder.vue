<template>
  <header
    class="max-w-6xl mx-auto mt-[36px] md:mt-[40px] mb-[12px] flex items-center justify-between"
  >
    <a href="./pages/home.html">
      <img src="./images/logo.png" alt="logo" class="mr-[12px] md:mr-0 w-[110px]" />
    </a>

    <div class="flex md:hidden drawer drawer-end items-end justify-end">
      <input id="navbar-drawer" type="checkbox" class="drawer-toggle" />
      <div class="drawer-content">
        <!-- Page content here -->
        <label for="navbar-drawer">
          <svg
            xmlns="http://www.w3.org/2000/svg"
            class="h-8 w-8 ml-[12px]"
            fill="none"
            viewBox="0 0 24 24"
            stroke="currentColor"
          >
            <path
              stroke-linecap="round"
              stroke-linejoin="round"
              stroke-width="2"
              d="M4 6h16M4 12h16M4 18h7"
            />
          </svg>
        </label>
      </div>
      <div class="drawer-side">
        <label for="navbar-drawer" class="drawer-overlay"></label>
        <ul class="menu p-4 w-60 h-full bg-base-200 text-base-content">
          <!-- Sidebar content here -->
          <li><router-link to="/" class="p-[16px]"> خانه </router-link></li>
          <li><a class="p-[16px]"> محصولات </a></li>
          <li><a class="p-[16px]"> اهداف </a></li>
          <li><a class="p-[16px]"> راهکارها </a></li>
          <li><a class="p-[16px]"> تازه‌ها </a></li>
          <li><a class="p-[16px]"> نمایندگی‌ها </a></li>
          <li><a class="p-[16px]"> درباره ما </a></li>
          <li>
            <router-link to="/contactUs" class="p-[16px]"> تماس با ما </router-link>
          </li>
          <li><a class="p-[16px]"> سوالات متداول </a></li>
        </ul>
      </div>
    </div>

    <div
      class="hidden md:flex items-center justify-end w-full mr-[22px] text-[16px] font-medium text-[#403D3D]"
    >
      <router-link to="/" class="p-[16px]"> خانه </router-link>
      <a class="p-[16px]"> محصولات </a>
      <a class="p-[16px]"> اهداف </a>
      <a class="p-[16px]"> راهکارها </a>
      <a class="p-[16px]"> تازه‌ها </a>
      <a class="p-[16px]"> نمایندگی‌ها </a>
      <a class="p-[16px]"> درباره ما </a>
      <router-link to="/contactUs" class="p-[16px]"> تماس با ما </router-link>
      <a class="p-[16px]"> سوالات متداول </a>
    </div>

    <!-- Header:End -->
  </header>
</template>

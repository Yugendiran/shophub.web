import type { NuxtLink } from '#build/components';
<template>
  <div>
    <div
      class="h-20 w-full bg-white shadow-xl flex justify-between items-center px-5"
    >
      <div>
        <img
          src="https://preview.colorlib.com/theme/ashion/img/logo.png.webp"
          alt=""
        />
      </div>
      <div>
        <div
          @click="isSidebarOpened = !isSidebarOpened"
          class="h-8 w-8 border-2 border-black rounded-md flex items-center justify-center lg:hidden"
        >
          <i class="fa-solid fa-bars"></i>
        </div>

        <ul class="hidden lg:flex gap-3 text-lg font-medium">
          <li v-for="(item, index) in menuItems" :key="index">
            <NuxtLink :to="item.route">{{ item.name }}</NuxtLink>
          </li>
        </ul>
      </div>
      <div class="hidden lg:block">
        <div class="flex items-center gap-3 mt-10 w-full justify-evenly">
          <NuxtLink to="/products">
            <div class="relative">
              <i class="fa-solid fa-magnifying-glass"></i>
            </div>
          </NuxtLink>
          <NuxtLink to="/wishlist">
            <div class="relative">
              <i class="fa-solid fa-heart"></i>
              <div
                class="absolute -top-2 -right-2 h-3 w-3 rounded-full bg-black text-white text-[8px] flex justify-center items-center font-medium"
              >
                2
              </div>
            </div>
          </NuxtLink>
          <NuxtLink to="/cart">
            <div class="relative">
              <i class="fa-solid fa-cart-shopping"></i>
              <div
                class="absolute -top-2 -right-2 h-3 w-3 rounded-full bg-black text-white text-[8px] flex justify-center items-center font-medium"
              >
                2
              </div>
            </div>
          </NuxtLink>

          <NuxtLink to="/profile">
            <div class="relative">
              <i class="fa-solid fa-user"></i>
            </div>
          </NuxtLink>
        </div>
      </div>
    </div>

    <div
      class="fixed top-0 h-screen bg-black/50 w-full overflow-hidden transition-[0.3s] lg:hidden"
      :class="isSidebarOpened ? 'left-0' : '-left-full'"
      ref="modal"
    >
      <div class="h-full w-[80%] max-w-[320px] bg-white p-5" ref="modalItem">
        <div class="flex justify-between items-center">
          <img
            src="https://preview.colorlib.com/theme/ashion/img/logo.png.webp"
            alt=""
          />
          <div
            @click="isSidebarOpened = !isSidebarOpened"
            class="h-10 w-10 rounded-full border border-black flex justify-center items-center"
          >
            <i class="fa-solid fa-xmark"></i>
          </div>
        </div>

        <div class="mt-5">
          <ul class="text-lg font-medium">
            <li v-for="(item, index) in menuItems" :key="index">
              <NuxtLink :to="item.route">{{ item.name }}</NuxtLink>
            </li>
          </ul>
        </div>

        <div class="flex items-center gap-3 mt-10 w-full justify-evenly">
          <NuxtLink to="/products">
            <div class="relative">
              <i class="fa-solid fa-magnifying-glass"></i>
            </div>
          </NuxtLink>
          <NuxtLink to="/wishlist">
            <div class="relative">
              <i class="fa-solid fa-heart"></i>
              <div
                class="absolute -top-2 -right-2 h-3 w-3 rounded-full bg-black text-white text-[8px] flex justify-center items-center font-medium"
              >
                2
              </div>
            </div>
          </NuxtLink>
          <NuxtLink to="/cart">
            <div class="relative">
              <i class="fa-solid fa-cart-shopping"></i>
              <div
                class="absolute -top-2 -right-2 h-3 w-3 rounded-full bg-black text-white text-[8px] flex justify-center items-center font-medium"
              >
                2
              </div>
            </div>
          </NuxtLink>

          <NuxtLink to="/profile">
            <div class="relative">
              <i class="fa-solid fa-user"></i>
            </div>
          </NuxtLink>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isSidebarOpened: false,
      menuItems: [
        {
          name: "Home",
          route: "/",
        },
        {
          name: "Categories",
          route: "/categories",
        },
        {
          name: "Products",
          route: "/products",
        },
        {
          name: "Contact",
          route: "/contact",
        },
      ],
    };
  },
  mounted() {
    window.addEventListener("click", (e) => {
      if (this.$refs.modal.contains(e.target)) {
        if (this.$refs.modalItem.contains(e.target)) {
          return;
        }

        this.isSidebarOpened = false;
      }
    });
  },
};
</script>

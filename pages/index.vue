<template>
  <div>
    <NavBar />

    <!-- Categories Section -->
    <section>
      <div class="grid w-full min-h-screen gap-4 lg:grid-cols-2">
        <div
          class="h-[300px] lg:h-full w-full bg-[#fae3d9] flex flex-col justify-center p-5"
        >
          <h1 class="mb-3 text-2xl font-bold">Women's Fashion</h1>
          <p class="mb-5 text-sm">
            Lorem ipsum dolor sit amet consectetur, adipisicing elit. Earum
            deleniti in qui quaerat animi ipsum corrupti sunt tempora
            necessitatibus fugiat?
          </p>
          <span
            class="font-medium underline decoration-2 decoration-red-500 underline-offset-8"
            >Shop Now</span
          >
        </div>
        <div class="grid w-full h-full gap-4 sm:grid-cols-2">
          <div
            class="h-[300px] lg:h-full w-full bg-[#bee2d6] flex flex-col justify-center p-5"
          >
            <h1 class="mb-3 text-2xl font-bold">Men's Fashion</h1>
            <p class="mb-5 text-sm">
              Lorem ipsum dolor sit amet consectetur, adipisicing elit. Earum
              deleniti in qui quaerat animi ipsum corrupti sunt tempora
              necessitatibus fugiat?
            </p>
            <span
              class="font-medium underline decoration-2 decoration-red-500 underline-offset-8"
              >Shop Now</span
            >
          </div>
          <div
            class="h-[300px] lg:h-full w-full bg-[#d6d3f0] flex flex-col justify-center p-5"
          >
            <h1 class="mb-3 text-2xl font-bold">Kid's Fashion</h1>
            <p class="mb-5 text-sm">
              Lorem ipsum dolor sit amet consectetur, adipisicing elit. Earum
              deleniti in qui quaerat animi ipsum corrupti sunt tempora
              necessitatibus fugiat?
            </p>
            <span
              class="font-medium underline decoration-2 decoration-red-500 underline-offset-8"
              >Shop Now</span
            >
          </div>
          <div
            class="h-[300px] lg:h-full w-full bg-[#fedbe4] flex flex-col justify-center p-5"
          >
            <h1 class="mb-3 text-2xl font-bold">Cosmetics</h1>
            <p class="mb-5 text-sm">
              Lorem ipsum dolor sit amet consectetur, adipisicing elit. Earum
              deleniti in qui quaerat animi ipsum corrupti sunt tempora
              necessitatibus fugiat?
            </p>
            <span
              class="font-medium underline decoration-2 decoration-red-500 underline-offset-8"
              >Shop Now</span
            >
          </div>
          <div
            class="h-[300px] lg:h-full w-full bg-[#cee2f5] flex flex-col justify-center p-5"
          >
            <h1 class="mb-3 text-2xl font-bold">Accessories</h1>
            <p class="mb-5 text-sm">
              Lorem ipsum dolor sit amet consectetur, adipisicing elit. Earum
              deleniti in qui quaerat animi ipsum corrupti sunt tempora
              necessitatibus fugiat?
            </p>
            <span
              class="font-medium underline decoration-2 decoration-red-500 underline-offset-8"
              >Shop Now</span
            >
          </div>
        </div>
      </div>
    </section>
    <!-- Categories Section -->

    <!-- Product List -->
    <section class="my-20">
      <div class="px-5 mx-auto max-w-7xl">
        <div class="items-center justify-between mb-5 md:flex">
          <h1 class="text-2xl font-bold">New Products</h1>
          <ul class="flex flex-wrap items-center gap-3 text-lg">
            <li
              class="underline decoration-2 decoration-red-500 underline-offset-8"
            >
              Women
            </li>
            <li>Men</li>
            <li>Kid</li>
            <li>Cosmetics</li>
            <li>Accessories</li>
          </ul>
        </div>
        <div class="bg-white">
          <div class="overflow-hidden">
            <h2 class="sr-only">Products</h2>

            <div
              class="grid grid-cols-2 -mx-px border-gray-200 sm:mx-0 md:grid-cols-3 lg:grid-cols-4"
            >
              <div
                v-for="n in 10"
                :key="n"
                class="relative p-4 border border-gray-200 group sm:p-6"
              >
                <div
                  class="overflow-hidden bg-gray-200 rounded-lg aspect-h-1 aspect-w-1 group-hover:opacity-75"
                >
                  <img
                    src="https://tailwindui.com/img/ecommerce-images/category-page-05-image-card-01.jpg"
                    alt="TODO"
                    class="object-cover object-center w-full h-full"
                  />
                </div>
                <div class="pt-10 pb-4 text-center">
                  <h3 class="text-sm font-medium text-gray-900">
                    <a href="#">
                      <span aria-hidden="true" class="absolute inset-0"></span>
                      Organize Basic Set (Walnut)
                    </a>
                  </h3>
                  <div class="flex flex-col items-center mt-3">
                    <p class="sr-only">5 out of 5 stars</p>
                    <div class="flex items-center">
                      <svg
                        class="flex-shrink-0 w-5 h-5 text-yellow-400"
                        viewBox="0 0 20 20"
                        fill="currentColor"
                        aria-hidden="true"
                      >
                        <path
                          fill-rule="evenodd"
                          d="M10.868 2.884c-.321-.772-1.415-.772-1.736 0l-1.83 4.401-4.753.381c-.833.067-1.171 1.107-.536 1.651l3.62 3.102-1.106 4.637c-.194.813.691 1.456 1.405 1.02L10 15.591l4.069 2.485c.713.436 1.598-.207 1.404-1.02l-1.106-4.637 3.62-3.102c.635-.544.297-1.584-.536-1.65l-4.752-.382-1.831-4.401z"
                          clip-rule="evenodd"
                        />
                      </svg>
                      <svg
                        class="flex-shrink-0 w-5 h-5 text-yellow-400"
                        viewBox="0 0 20 20"
                        fill="currentColor"
                        aria-hidden="true"
                      >
                        <path
                          fill-rule="evenodd"
                          d="M10.868 2.884c-.321-.772-1.415-.772-1.736 0l-1.83 4.401-4.753.381c-.833.067-1.171 1.107-.536 1.651l3.62 3.102-1.106 4.637c-.194.813.691 1.456 1.405 1.02L10 15.591l4.069 2.485c.713.436 1.598-.207 1.404-1.02l-1.106-4.637 3.62-3.102c.635-.544.297-1.584-.536-1.65l-4.752-.382-1.831-4.401z"
                          clip-rule="evenodd"
                        />
                      </svg>
                      <svg
                        class="flex-shrink-0 w-5 h-5 text-yellow-400"
                        viewBox="0 0 20 20"
                        fill="currentColor"
                        aria-hidden="true"
                      >
                        <path
                          fill-rule="evenodd"
                          d="M10.868 2.884c-.321-.772-1.415-.772-1.736 0l-1.83 4.401-4.753.381c-.833.067-1.171 1.107-.536 1.651l3.62 3.102-1.106 4.637c-.194.813.691 1.456 1.405 1.02L10 15.591l4.069 2.485c.713.436 1.598-.207 1.404-1.02l-1.106-4.637 3.62-3.102c.635-.544.297-1.584-.536-1.65l-4.752-.382-1.831-4.401z"
                          clip-rule="evenodd"
                        />
                      </svg>
                      <svg
                        class="flex-shrink-0 w-5 h-5 text-yellow-400"
                        viewBox="0 0 20 20"
                        fill="currentColor"
                        aria-hidden="true"
                      >
                        <path
                          fill-rule="evenodd"
                          d="M10.868 2.884c-.321-.772-1.415-.772-1.736 0l-1.83 4.401-4.753.381c-.833.067-1.171 1.107-.536 1.651l3.62 3.102-1.106 4.637c-.194.813.691 1.456 1.405 1.02L10 15.591l4.069 2.485c.713.436 1.598-.207 1.404-1.02l-1.106-4.637 3.62-3.102c.635-.544.297-1.584-.536-1.65l-4.752-.382-1.831-4.401z"
                          clip-rule="evenodd"
                        />
                      </svg>
                      <svg
                        class="flex-shrink-0 w-5 h-5 text-yellow-400"
                        viewBox="0 0 20 20"
                        fill="currentColor"
                        aria-hidden="true"
                      >
                        <path
                          fill-rule="evenodd"
                          d="M10.868 2.884c-.321-.772-1.415-.772-1.736 0l-1.83 4.401-4.753.381c-.833.067-1.171 1.107-.536 1.651l3.62 3.102-1.106 4.637c-.194.813.691 1.456 1.405 1.02L10 15.591l4.069 2.485c.713.436 1.598-.207 1.404-1.02l-1.106-4.637 3.62-3.102c.635-.544.297-1.584-.536-1.65l-4.752-.382-1.831-4.401z"
                          clip-rule="evenodd"
                        />
                      </svg>
                    </div>
                    <p class="mt-1 text-sm text-gray-500">38 reviews</p>
                  </div>
                  <p class="mt-4 text-base font-medium text-gray-900">$149</p>
                </div>
              </div>

              <!-- More products... -->
            </div>
          </div>
        </div>
      </div>
    </section>
    <!-- Product List -->

    <!-- Offers Section -->
    <section>
      <div class="w-full h-auto bg-red-100 swiper offersSwiper">
        <div class="swiper-wrapper">
          <div
            v-for="n in 5"
            :key="n"
            class="flex flex-col items-center justify-center p-5 text-center swiper-slide"
          >
            <p class="mb-5 font-medium">Best Collection {{ n }}</p>
            <h1 class="mb-5 text-2xl font-bold text-center">
              Get 50% off on your first order
            </h1>
            <span
              class="font-medium underline decoration-2 decoration-red-500 underline-offset-8"
              >Shop Now</span
            >
          </div>
        </div>
      </div>
    </section>
    <!-- Offers Section -->
  </div>
</template>

<script>
export default {
  data() {
    return {
      swipers: {
        offersSwiper: null,
      },
    };
  },
  mounted() {
    this.swipers.offersSwiper = new window.Swiper(".offersSwiper", {
      autoplay: {
        delay: 1000,
        disableOnInteraction: false,
      },
    });
  },
};
</script>

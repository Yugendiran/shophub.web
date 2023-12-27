<template>
  <div>
    <NavBar />

    <!-- Categories Section -->
    <section>
      <div class="w-full min-h-screen grid lg:grid-cols-2 gap-4">
        <div
          class="h-[300px] lg:h-full w-full bg-[#fae3d9] flex flex-col justify-center p-5"
        >
          <h1 class="text-2xl mb-3 font-bold">Women's Fashion</h1>
          <p class="text-sm mb-5">
            Lorem ipsum dolor sit amet consectetur, adipisicing elit. Earum
            deleniti in qui quaerat animi ipsum corrupti sunt tempora
            necessitatibus fugiat?
          </p>
          <span
            class="font-medium underline decoration-2 decoration-red-500 underline-offset-8"
            >Shop Now</span
          >
        </div>
        <div class="grid sm:grid-cols-2 h-full w-full gap-4">
          <div
            class="h-[300px] lg:h-full w-full bg-[#bee2d6] flex flex-col justify-center p-5"
          >
            <h1 class="text-2xl mb-3 font-bold">Men's Fashion</h1>
            <p class="text-sm mb-5">
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
            <h1 class="text-2xl mb-3 font-bold">Kid's Fashion</h1>
            <p class="text-sm mb-5">
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
            <h1 class="text-2xl mb-3 font-bold">Cosmetics</h1>
            <p class="text-sm mb-5">
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
            <h1 class="text-2xl mb-3 font-bold">Accessories</h1>
            <p class="text-sm mb-5">
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
        <div class="md:flex items-center justify-between mb-5">
          <h1 class="text-2xl font-bold">New Products</h1>
          <ul class="flex items-center text-lg gap-3 flex-wrap">
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
              class="-mx-px grid grid-cols-2 border-gray-200 sm:mx-0 md:grid-cols-3 lg:grid-cols-4"
            >
              <div
                v-for="n in 10"
                :key="n"
                class="group relative border border-gray-200 p-4 sm:p-6"
              >
                <div
                  class="aspect-h-1 aspect-w-1 overflow-hidden rounded-lg bg-gray-200 group-hover:opacity-75"
                >
                  <img
                    src="https://tailwindui.com/img/ecommerce-images/category-page-05-image-card-01.jpg"
                    alt="TODO"
                    class="h-full w-full object-cover object-center"
                  />
                </div>
                <div class="pb-4 pt-10 text-center">
                  <h3 class="text-sm font-medium text-gray-900">
                    <a href="#">
                      <span aria-hidden="true" class="absolute inset-0"></span>
                      Organize Basic Set (Walnut)
                    </a>
                  </h3>
                  <div class="mt-3 flex flex-col items-center">
                    <p class="sr-only">5 out of 5 stars</p>
                    <div class="flex items-center">
                      <svg
                        class="text-yellow-400 h-5 w-5 flex-shrink-0"
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
                        class="text-yellow-400 h-5 w-5 flex-shrink-0"
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
                        class="text-yellow-400 h-5 w-5 flex-shrink-0"
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
                        class="text-yellow-400 h-5 w-5 flex-shrink-0"
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
                        class="text-yellow-400 h-5 w-5 flex-shrink-0"
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
      <div class="h-auto w-full bg-red-100 swiper offersSwiper">
        <div class="swiper-wrapper">
          <div
            v-for="n in 5"
            :key="n"
            class="p-5 text-center flex justify-center items-center flex-col swiper-slide"
          >
            <p class="font-medium mb-5">Best Collection {{ n }}</p>
            <h1 class="text-2xl font-bold text-center mb-5">
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

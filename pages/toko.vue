<template>
  <Header></Header>
  <div>
    <div class="bg-white">
      <div class="mx-auto max-w-2xl px-4 py-16 sm:px-6 sm:py-24 lg:max-w-7xl lg:px-8">
        <h2 class="sr-only">Products</h2>
        <div class="grid grid-cols-1 gap-x-6 gap-y-10 sm:grid-cols-2 lg:grid-cols-3 xl:grid-cols-4 xl:gap-x-8">
          <div v-for="product in products" :key="product.id">
            <nuxt-link :to="`/products/${product.id}`">
              <a class="group">
                <div class="aspect-h-1 aspect-w-1 w-full overflow-hidden rounded-lg bg-gray-200 xl:aspect-h-8 xl:aspect-w-7">
                  <img :src="product.imageSrc" :alt="product.imageAlt" class="h-full w-full object-cover object-center group-hover:opacity-75" />
                </div>
                <!-- <h3 class="mt-4 text-sm text-gray-700">{{ product.name }}</h3>
                <p class="mt-1 text-lg font-medium text-pink-500">Rp {{ product.price }}</p> -->
                <a href="#">
                  <h5 class="text-xl tracking-tight text-slate-900">{{ product.name }}</h5>
                </a>
                <div class="mt-2 mb-5 flex items-center justify-between">
                  <p>
                    <span class="mt-1 text-lg font-medium text-pink-500">Rp {{ product.price }}</span>
                    <!-- <span class="text-sm text-slate-900 line-through">$699</span> -->
                  </p>
                </div>
              </a>
            </nuxt-link>
            <button class="flex items-center justify-center bg-gray-900 px-2 py-1 text-sm text-white transition hover:bg-gray-700">
              <svg xmlns="http://www.w3.org/2000/svg" class="mr-2 h-5 w-5" viewBox="0 0 20 20" fill="currentColor">
                <path
                  d="M3 1a1 1 0 000 2h1.22l.305 1.222a.997.997 0 00.01.042l1.358 5.43-.893.892C3.74 11.846 4.632 14 6.414 14H15a1 1 0 000-2H6.414l1-1H14a1 1 0 00.894-.553l3-6A1 1 0 0017 3H6.28l-.31-1.243A1 1 0 005 1H3zM16 16.5a1.5 1.5 0 11-3 0 1.5 1.5 0 013 0zM6.5 18a1.5 1.5 0 100-3 1.5 1.5 0 000 3z"
                />
              </svg>
              <nuxt-link to="/cart">Add to cart</nuxt-link>
            </button>
          </div>
        </div>
      </div>
    </div>
  </div>
  <chat></chat>
</template>

<script>
import { products } from '~/data/products.js';
export default {
  data() {
    return {
      products: [],
    };
  },
  mounted() {
    this.products = products;
  },
};
</script>

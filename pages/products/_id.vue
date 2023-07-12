<template>
  <div>
    <h2>{{ product.id }}</h2>
    <h2>{{ product.name }}</h2>
    <p>{{ product.description }}</p>
    <!-- Tampilkan informasi produk lainnya -->
  </div>
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
  async asyncData({ params }) {
    // Di sini Anda dapat mengambil data produk dari sumber data eksternal, seperti API
    const productId = params.id;
    // Misalnya, dapatkan data produk berdasarkan ID dari API

    return {
      product,
    };
  },
};
</script>

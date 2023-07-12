<template>
  <Header></Header>
  <div class="mx-20">
    <section class="bg-center rounded-lg h-auto max-w-full bg-contain bg-[url('https://mynorthwest.com/wp-content/uploads/2019/12/thrift-store-unsplash-620.jpg')] bg-gray-700 bg-blend-multiply">
      <div class="px-4 mx-auto max-w-screen-xl text-center py-24 lg:py-56">
        <h1 class="mb-4 text-4xl font-extrabold tracking-tight leading-none text-pink-500 md:text-5xl lg:text-6xl">Thrifly</h1>
        <h1 class="mb-4 text-4xl font-extrabold tracking-tight leading-none text-white md:text-5xl lg:text-6xl">Mau bergaya tapi kurang biaya !?</h1>
        <p class="mb-8 text-lg font-normal text-gray-300 lg:text-xl sm:px-16 lg:px-48">Temukan Barang Bekas Berkualitas dengan Harga Terjangkau - Pengalaman Belanja Serba Hemat di Thrifly.</p>
        <div class="flex flex-col space-y-4 sm:flex-row sm:justify-center sm:space-y-0 sm:space-x-4">
          <a href="#" class="inline-flex justify-center items-center py-3 px-5 text-base font-medium text-center text-black rounded-lg bg-gray-100 hover:bg-pink-500">
            <nuxt-link to="/toko">Ke Toko</nuxt-link>
            <svg class="w-3.5 h-3.5 ml-2" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 14 10">
              <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M1 5h12m0 0L9 1m4 4L9 9" />
            </svg>
          </a>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped></style>

<template>
  <div>
    <div class="grid grid-cols-4 gap-5">
      <div v-for="p in products">
        <productCard :product="p" />
      </div>
    </div>
  </div>
</template>

<script setup>
definePageMeta({
  layout: "products",
});

// Fetch the Products
const { data: products } = await useFetch("https://fakestoreapi.com/products/");
useHead({
  title: "FakeStore | Products",
  meta: [
    {
      name: "description",
      content: "FakeStore | Products Nuxt 3",
    },
  ],
});
</script>

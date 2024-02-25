<template>
  <div>
    <productDetails :product="products" />
  </div>
</template>

<script setup>
const { id } = useRoute().params;
const url = "https://fakestoreapi.com/products/" + id;

// Fetch the Products
const { data: products } = await useFetch(url, { key: id });

if (!products.value) {
  throw createError({ statusCode: 404, statusMessage: "Product not found" });
}

definePageMeta({
  layout: "products",
});
</script>

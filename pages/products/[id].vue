<template>
  <div>
    <Head>
      <Title>FakeStore | {{ products.title }}</Title>
      <Meta name="description" :content="products.description"></Meta>
    </Head>
    <productDetails :product="products" />
  </div>
</template>

<script setup>
const { id } = useRoute().params;
const url = "https://fakestoreapi.com/products/" + id;

// Fetch the Products
const { data: products } = await useFetch(url, { key: id });

if (!products.value) {
  throw createError({
    statusCode: 404,
    statusMessage: "Product not found",
    fatal: true,
  });
}

definePageMeta({
  layout: "products",
});
</script>

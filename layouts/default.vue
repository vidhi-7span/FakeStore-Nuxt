<template>
  <div>
    <header class="shadow-md bg-white">
      <nav class="container mx-auto p-4 flex justify-between item-center">
        <NuxtLink to="/" class="font-bold">FakeStore</NuxtLink>
        <ul class="flex gap-4">
          <li>
            <NuxtLink to="/">Home</NuxtLink>
          </li>
          <li>
            <NuxtLink to="/about">About</NuxtLink>
          </li>
          <li>
            <NuxtLink to="/products" class="btn">Products</NuxtLink>
          </li>
        </ul>
      </nav>
    </header>

    <!-- Other page Content -->
    <div class="container mx-auto p-4">
      <slot />
    </div>
  </div>
</template>

<style scoped>
.router-link-exact-active {
  color: green;
}
</style>

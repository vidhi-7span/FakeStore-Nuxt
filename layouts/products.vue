<template>
  <div>
    <header class="shadow-md bg-white">
      <nav class="container mx-auto p-4 flex justify-between item-center">
        <NuxtLink to="/products" class="font-bold">FakeStore Products</NuxtLink>
      </nav>
    </header>

    <!-- Other page Content -->
    <div class="container mx-auto p-4">
      <slot />
    </div>

    <footer class="container mx-auto p-5 flex justify-between border-t-2">
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
    </footer>
  </div>
</template>

<style scoped></style>

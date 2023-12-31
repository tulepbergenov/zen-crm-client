<script setup lang="ts">
import { ref } from "vue";
const links = ref([
  { id: 1, label: "Home", url: "" },
  { id: 2, label: "Products", url: "products" },
  { id: 3, label: "Payments", url: "payments" },
  { id: 4, label: "Orders", url: "orders" },
  { id: 5, label: "Customers", url: "customers" },
  { id: 6, label: "Feedback", url: "feedback" },
  { id: 7, label: "Settings", url: "settings" },
  { id: 8, label: "Help", url: "help" },
]);
</script>

<template>
  <aside class="px-10 py-6">
    <nav>
      <NuxtLink
        to="/"
        class="inline-block text-3xl font-black text-app-clr-primary underline transition-colors duration-200 ease-in-out hover:text-blue-500"
        >Zen</NuxtLink
      >
      <ul class="mt-10 flex flex-col gap-y-5">
        <li v-for="link of links" :key="link.id" class="flex">
          <NuxtLink
            :to="`/${link.url}`"
            class="inline-block transition-colors duration-200 ease-in-out hover:text-app-clr-primary hover:underline"
            >{{ link.label }}</NuxtLink
          >
        </li>
      </ul>
    </nav>
  </aside>
</template>

<script setup lang="ts">
import { RouterLink } from "vue-router";
let id = 0;
const navBarItems = [
  { id: id++, name: "Home", value: "/" },
  { id: id++, name: "Explore", value: "/explore" },
  { id: id++, name: "Activity", value: "/activiy" },
  { id: id++, name: "Comunity", value: "/comunity;" },
  { id: id++, name: "About", value: "/about" },
];
</script>

<template>
  <div class="flex items-center justify-evenly">
    <img alt="Vue logo" height="40" width="40" src="@/assets/logo.svg" />
    <div class="flex items-center justify-center">
      <RouterLink
        v-for="navBarItem in navBarItems"
        :key="navBarItem"
        :to="navBarItem.value"
        >{{ navBarItem.name }}</RouterLink
      >
    </div>
    <div class="font-bold">Search</div>
  </div>
</template>

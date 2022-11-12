<template>
  <HelloWorld
    :items="items"
  />
</template>

<script setup lang="ts">
import HelloWorld from './components/HelloWorld.vue'
import type User from "@/types/User";
import {ref} from "vue";

const items = ref<User[]>([
  {
    name: "Nord",
    age: 18
  },
  {
    name: "Coders",
    age: 81
  }
]);
</script>

<template>
  <div
    v-for="item in items"
  >
    <span
      v-text="item.name"
    >
    </span>

    <span
        v-text="item.age"
    >
    </span>
  </div>
</template>

<script setup lang="ts">
  import {ref} from "vue";
  import type User from "@/types/User";

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
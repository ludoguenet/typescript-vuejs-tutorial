<template>
  <div
    v-for="item in props.items"
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
  import type User from "@/types/User";

  const props = defineProps<{
    items: User[],
  }>();
</script>
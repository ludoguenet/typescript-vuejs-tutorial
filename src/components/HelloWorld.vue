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

  <button
    v-on:click="display('name')"
  >
    Display Name
  </button>

  <button
      v-on:click="display('age')"
  >
    Display Age
  </button>
</template>

<script setup lang="ts">
  import type User from "@/types/User";
  import type UserProperty from "@/types/UserType";

  const props = defineProps<{
    items: User[],
  }>();

  const display = (property: UserProperty) => {
    props.items.forEach((item: User) => {
      console.log(item[property]);
    });
  }
</script>
<script setup lang="ts">
import { useFetch } from 'nuxt3/dist/app/composables';
import { ref } from 'vue';
const count = ref(0);

const { data }: { data: any } = await useFetch("api/hello?search=girls");
</script>
<template>
  <div>
    <div>Todo</div>
    <h2>Counter</h2>
    {{ count }}
    <button @click="count++">Push</button>
    {{ data }}
  </div>
</template>

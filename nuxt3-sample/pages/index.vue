<script setup lang="ts">
import { useFetch } from "nuxt3/dist/app/composables";
import { ref } from "vue";
const count = ref(0);

const { data }: { data: any } = await useFetch("api/hello?search=girls", {
  pick: ["score"],
});
</script>
<template>
  <div>
    {{ data }}
  </div>
</template>

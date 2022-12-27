<script setup>
  import TheWelcome from "../components/TheWelcome.vue";
  import {watch} from 'vue';
  import { useRoute } from 'vue-router';
  import router from '../router';

  const route = useRoute();
  console.log(route.fullPath);
</script>

<template>
  <main>
    <TheWelcome />
  </main>
</template>

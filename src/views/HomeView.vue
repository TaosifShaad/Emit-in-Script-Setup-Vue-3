<template>
  <main>
    <TheWelcome/>
  </main>
</template>

<script setup>
  import TheWelcome from "../components/TheWelcome.vue";
  import {watch, ref} from 'vue';
  import { useRoute } from 'vue-router';
  import router from '../router';
  import { provide } from "vue";
  import { user } from "@/stores/userStore"

  let name = ref('john doe')
  provide('name', name.value)

  const route = useRoute();
  // console.log(route.fullPath);
</script>
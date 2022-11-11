<script setup lang="ts">
import { ref } from "vue";
import { storeToRefs } from "pinia";
import { useCounterStore } from "../store/counter";
defineProps<{ msg: string }>();

const { count } = storeToRefs(useCounterStore());
</script>

<template>
  <h1 class="text-2xl mb-4 font-bold">{{ msg }}</h1>

  <button type="button" @click="count++" class=" py-2 px-4 bg-blue-500 rounded-full">count is: {{ count }}</button>
  <!-- <p>
    <router-link to="/" class="">Go to index</router-link>
    <router-link to="/home" class="routerlink">Go to Home</router-link>
    <router-link to="/about" class="routerlink">Go to About</router-link>
  </p> -->
  <!-- <router-view /> -->
</template>

<style scoped>
a {
  color: #42b983;
}

label {
  margin: 0 0.5em;
  font-weight: bold;
}

code {
  background-color: #eee;
  padding: 2px 4px;
  border-radius: 4px;
  color: #304455;
}
.routerlink {
  margin: 0 10px;
}
</style>

<script setup lang="ts">
import { ref } from "vue";

import BaseInput from "./components/BaseInput.vue";
const input = ref("");
</script>

<template>
  <form>
    <BaseInput label="Input" v-model="input" />
    <div>{{ input }}</div>
  </form>
</template>

<style></style>

<script setup lang="ts">
import { ref } from "vue";

import BaseInput from "./components/BaseInput.vue";
const form = ref({
  input: "",
});
</script>

<template>
  <form>
    <BaseInput type="text" label="Input" v-model="form.input" />
    <div>{{ form.input }}</div>
  </form>
</template>

<style></style>

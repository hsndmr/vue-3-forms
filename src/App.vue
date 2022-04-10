<script setup lang="ts">
import { ref } from "vue";

import BaseInput from "./components/BaseInput.vue";
import BaseSelect from "./components/BaseSelect.vue";
const form = ref({
  input: "",
  select: "a",
});
const options = ref(["a", "b"]);
</script>

<template>
  <form>
    <!-- Base Input -->
    <BaseInput type="text" label="Input" v-model="form.input" />
    <div>{{ form.input }}</div>
    <br />
    <!-- Base Select -->
    <BaseSelect
      label="Select"
      v-model="form.select"
      :options="(options as any)"
    />
    <div>{{ form.select }}</div>
    <br />
  </form>
</template>

<style></style>

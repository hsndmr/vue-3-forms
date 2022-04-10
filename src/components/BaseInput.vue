<script setup lang="ts">
defineProps<{
  label?: string;
  modelValue?: string;
}>();
</script>

<template>
  <label>{{ label }}</label>
  <br />
  <input
    v-bind="$attrs"
    :placeholder="(label as any)"
    class="form-input"
    :value="modelValue"
    @input="$emit('update:modelValue', ($event as any).target.value)"
  />
</template>

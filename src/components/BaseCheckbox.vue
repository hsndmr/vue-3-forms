<script setup lang="ts">
defineProps<{
  label?: string;
  modelValue?: boolean;
}>();
</script>
<template>
  <input
    type="checkbox"
    :checked="(modelValue as any)"
    @change="$emit('update:modelValue', ($event as any).target.checked)"
  />
  <label v-if="label">{{ label }}</label>
</template>

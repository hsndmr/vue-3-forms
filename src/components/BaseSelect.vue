<script setup lang="ts">
defineProps<{
  label?: string;
  modelValue?: string;
  options: string[];
}>();
</script>

<template>
  <label v-if="label">{{ label }}</label>
  <select
    :value="modelValue"
    class="form-input"
    v-bind="{
      // @ts-ignore
      ...$attrs,
      onChange: ($event) => {
        $emit('update:modelValue', ($event as any).target.value);
      },
    }"
  >
    <option
      :key="(option as any)"
      v-for="option in options"
      :value="option"
      :selected="option === modelValue"
    >
      {{ option }}
    </option>
  </select>
</template>

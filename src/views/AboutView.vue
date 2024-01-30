<template>
  <div class="about">
    <label>組件AboutView</label>
    <input
      type="text"
      :value="props.modelValue"
      @input="emits('update:modelValue', $event.target.value)"
    />
  </div>
</template>

<script setup lang="ts">
import { defineProps, defineEmits } from "vue";
const props = defineProps(["modelValue"]);
const emits = defineEmits(["update:modelValue"]);
</script>

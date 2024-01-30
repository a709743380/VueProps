<template>
  <div class="about">
    <label>組件AboutViewOP</label>
    <input key="input1" :value="modelValue" @input="emitValue" />
    <!-- <button @click="sendMessage">Click</button> -->
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  props: {
    modelValue: String,
    modelModifiers: {
      default: () => ({}),
    },
  },
  emits: ["update:modelValue"],
  methods: {
    emitValue(e: InputEvent) {
      this.$emit("update:modelValue", (e.target as HTMLInputElement).value);
    },
  },
});
</script>

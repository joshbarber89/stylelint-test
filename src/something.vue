<!-- MyButton.vue -->
<template>
  <button class="__my---button" @click="handleClick">
    {{ label }}
  </button>
</template>

<script setup>
import { defineProps, defineEmits } from "vue";

// Define the props that the component accepts
const props = defineProps({
  label: {
    type: String,
    default: "Click Me",
  },
});

// Define the custom events the component can emit
const emit = defineEmits(["click"]);

// Method to handle the native button click and emit a custom event
const handleClick = () => {
  emit("click");
};
</script>

<style scoped>
.__my---button {
  background-color: #fff; /* Green background */
  border: none;
  color: white;
  padding: 10px 20px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
  margin: 4px 2px;
  cursor: pointer;
  border-radius: 8px;
  transition: background-color 0.3s;
}

.__my---button:hover {
  background-color: #45a049;
}
</style>

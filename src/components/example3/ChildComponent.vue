<template>
  <div>
    <p>{{ message }}</p>
    <button @click="emit('custom-event', 'Hello from child')">Send Event</button>
  </div>
</template>

<script setup>
import { defineProps, defineEmits } from 'vue';

const props = defineProps({
  message: {
    type: String,
    required: true
  }
});

const emit = defineEmits(['custom-event']);
</script>
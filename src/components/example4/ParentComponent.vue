<template>
  <div>
    <ChildComponent1 />
  </div>
</template>

<script setup>
import { provide, ref } from 'vue';
import ChildComponent1 from "@/components/example4/ChildComponent1.vue";

const sharedMessage = ref('Hello from provide');
provide('sharedMessage', sharedMessage);
</script>
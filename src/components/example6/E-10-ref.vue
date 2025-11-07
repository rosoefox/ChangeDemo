<template>
  <div>
    <p>Count: {{ count }}</p>
    <button @click="increment">Increment</button>
  </div>
</template>

<script setup>
import { ref, defineOptions } from 'vue';

defineOptions({
  name: 'E10Ref'
});

const count = ref(0);

const increment = () => {
  count.value++;
};
</script>
<template>
  <div>
    <p>Name: {{ person.name }}</p>
    <p>Age: {{ person.age }}</p>
    <button @click="incrementAge">Increment Age</button>
  </div>
</template>

<script setup>
import { reactive, defineOptions } from 'vue';

defineOptions({
  name: 'E11Reactive'
});

const person = reactive({
  name: 'John Doe',
  age: 30
});

const incrementAge = () => {
  person.age++;
};
</script>

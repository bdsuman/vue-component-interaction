<script setup>
import { reactive,ref } from 'vue'
import ChildComponent from './ChildComponent.vue';

const persons = reactive({
  'name'  : 'Suman',
  'age'   : 26,
  'message'   : 'hey im a web developer with 4 years of experience'
});
</script>

<template>
  <div class="mt-10">
    <h1 class="text-black-900 text-xl my-5">Parent Component:</h1>
    <h2 class="text-black text-l ">Name : {{ persons.name }}</h2>
    <h2 class="text-black text-l ">Age : {{ persons.age }}</h2>
    <h2 class="text-black text-l ">Message : {{ persons.message }}</h2>
  </div>

  <ChildComponent v-model:message="persons.message" ></ChildComponent>
</template>

<style scoped>

</style>
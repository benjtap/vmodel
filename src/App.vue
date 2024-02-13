<script setup>
  import Controller from './components/Controller.vue';
  import { reactive } from 'vue'; 
  const object1 = reactive({name: "Bruce", age: 38});
  const object2 = reactive({name: "Alex", age: 6});
</script>

<template>
  <div>
    {{object1}}<br/>
    {{object2}}
    <Controller :my-object="object1"/>
    <Controller :my-object="object2"/>
  </div>
</template>
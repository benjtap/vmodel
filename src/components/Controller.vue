<script setup>
  import { computed } from 'vue'

  const props = defineProps({
    myObject: {
      type: Object,
      default: () => {}
    }
  })

  const name = computed({
    get () {
      return props.myObject.name
    },
    set (value) {
     props.myObject.name = value
    }
  })

  const age = computed({
    get () {
      return props.myObject.age
    },
    set (value) {
     props.myObject.age = parseInt(value)
    }
  })
</script>

<template>
  <div>
    <input v-model="name"/><br/>
    <input v-model="age" type="number"/>
  </div>
</template>
<template>
  <div class="">
    Home
    <p>{{ text }}</p>
    <p>{{ counter }}</p>

  </div>
</template>

<script>
import { ref } from 'vue'
//permite crear una referencia reactiva a una variable

export default {
  setup() {
    const text = ref('Hola Crack')
    const counter = ref(0)

    setInterval(() => counter.value++, 500)
    
    return {
      text,
      counter,
    }
  }
}
</script>
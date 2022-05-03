<template>
  <div class="">
    Home
  <p>{{firstName}} {{lastName}} / dos variables</p>
  <p>{{fullName}} / funcion computed</p>
  <p>{{username}} / provide-inject</p>
  <button ref="btn">Click</button>

  </div>
</template>

<script setup>
import {defineProps, defineExpose ,ref ,toRefs,computed, inject, watch} from 'vue'
//Forma de usar props

  const props = defineProps({
    firstName: String,
    lastName: String,
  })

  const username = inject('username')
    
  const {firstName, lastName} =toRefs(props)
    
  const fullName = computed(()=>{
    return `${firstName.value} ${lastName.value}`
  })

  defineExpose({
    fullName,
  })

  const btn = ref(null)

  watch(btn, (valor)=>{
    console.log(valor)
  })
    
</script>
<template>
  <div class="">
    Home
  <p>{{firstName}} {{lastName}} / dos variables</p>
  <p>{{fullName}} / funcion computed</p>
  <p>{{username}} / provide-inject</p>
  <button ref="btn">Click</button>

  </div>
</template>

<script>
import {ref ,toRefs,computed, inject, watch} from 'vue'
//Forma de usar props


export default {

  props:{
    firstName: String,
    lastName: String,
  },

  setup(props, {expose}) {

    const username = inject('username')
    
    const {firstName, lastName} =toRefs(props)
    
    const fullName = computed(()=>{
      return `${firstName.value} ${lastName.value}`
    })

    expose({
      fullName,
    })

    const btn = ref(null)

    watch(btn, (valor)=>{
      console.log(valor)
    })
    
    return {
     fullName,
     username,
     btn
    }
  }
}
</script>
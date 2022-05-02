<template>
  <div class="">
    Home
  <p>{{firstName}} {{lastName}} / dos variables</p>
  <p>{{fullName}} / funcion computed</p>
  <p>{{username}} / provide-inject</p>

  </div>
</template>

<script>
import {toRefs,computed, inject} from 'vue'
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
    
    return {
     fullName,
     username
    }
  }
}
</script>
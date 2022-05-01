<template>
  <div class="">
    Home
  <p>{{firstName}} {{lastName}} / dos variables</p>
  <p>{{fullName}} / funcion computed</p>
  </div>
</template>

<script>
import {ref, computed} from 'vue'

export default {
  setup() {
    const firstName = ref('Jose')
    const lastName = ref('Morales')
    
    const fullName = computed(()=>{
      return `${firstName.value} ${lastName.value}`
    })

    return {
     firstName,
     lastName,
     fullName
    }
  }
}
</script>
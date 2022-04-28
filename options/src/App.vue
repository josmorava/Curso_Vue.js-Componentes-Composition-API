<template>
  <div class="">
    <ModalComponent />
    {{texto}}
  </div>

</template>

<script>
//import MenuComponent from './components/MenuComponent.vue'
import ModalComponent from './components/ModaComponent.vue'
import base from './mixins/base'


export default {
  name: 'App',
  mixins:[base],
  components: {
    ModalComponent,
  },
}

</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
/*-enter , -leave*/
/*-from , -active , -to*/


.fade-enter-from,
.fade-leave-to{
  opacity:0;
}

.fade-leave-active,
.fade-enter-active{
  transition: opacity 0.5s ease;
}
</style>

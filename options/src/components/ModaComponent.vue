<template>
  <div class="">
    <button @click="toggle">
      Modal
    </button>
    <teleport to='body' >
      <div v-show="show" class="modal">
        <h1>Titulo</h1>
        <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Est eligendi ex commodi fugiat similique ratione harum recusandae. At eligendi praesentium exercitationem maxime adipisci, magni, earum, libero impedit deleniti enim totam!</p>
        <button @click="toggle">
          Cerrar
        </button>  
      </div>
    </teleport>
    
  </div>
</template>

<script>
export default {
  data(){
    return{
      show: false
    }
  },
  methods: {
    toggle(){
      this.show = !this.show
    }
  },
}
</script>
<template>
  <div class="">
    {{ user }} Repositories
  </div>
</template>

<script>
export default {
  props: {
    user:{
      type: String,
      required: true,
    },
  },
  setup(props, ctx){
    //Se comporta como un hook de ciclo de vida, se ejecuta antes 
  },
  data(){
    return{
      repositories: [],
      filters: {},
      searchQuery: "",
    }
  },
  computed:{
    filteredRepositories(){
      return null
    },
    repositoriesMatchingSearchQuery(){
      return null
    },
  },
}
</script>
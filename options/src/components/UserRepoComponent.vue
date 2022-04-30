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
  setup(){
    //Se comporta como un hook de ciclo de vida, se ejecuta antes
    return{
      //repositories,
    }
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
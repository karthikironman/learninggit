<template>
  <div id="app">

  <input v-model="name">  
  
  </div>
</template>

<script>

export default {
  name: 'app',
  components: {
   
  },
  data(){
    return{
      decider:true,
      scpt:"<h1>this is a heading!</h1>",
     d : new Date(),
     info:'',
     loading: true,
     errored: false,
     name:''
    }
  },
 mounted() {
   if(localStorage.name){
     this.name = localStorage.name;
   }
 },
 watch:{
   name(newName){
     localStorage.name = newName;
   }
 }

}
</script>

<style>
.one{
  color:red;
  
}
</style>

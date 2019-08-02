<template>
<div class="outer"> 
  <div  class="s" style="font-family: 'Lacquer', sans-serif; ">{{info.data.contents.quotes[0].quote}}</div>
</div>


</template>

<script>

import axios from 'axios';
export default {
  name: 'app',
  components: {
   
  },
  data(){
    return{
    info: "inbd",
      
    }
  },
 
mounted () {
    axios
      .get( 'http://quotes.rest/qod.json?category=inspire ')
      .then(response => (this.info = response))
  },


}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Lacquer&display=swap');
.one{
  color:red;
  
}
.s{
  font-size: 60px;
  text-align: center;
  width:80%;
  height:80%;

  margin: auto;
  margin-top:10%;
  
 
}
.outer{
background-color: #F7CA18;
width:100%;
height:100%;
margin:0;
}
</style>

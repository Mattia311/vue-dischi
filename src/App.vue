<template>
  <div id="app">
    
  </div>
</template>

<script>
import axios from 'axios';


export default {
  name: 'App',
  components: {
   
  },
  mounted () {
    axios
    .get('https://flynn.boolean.careers/exercises/api/array/music')
    .then(r =>{
      console.log(r);
    }).catch(e=>{
      console.log(e, 'ERROR');
    })
  }
}
</script>

<style lang="scss">
@import "../node_modules/bootstrap/scss/bootstrap.scss";

</style>

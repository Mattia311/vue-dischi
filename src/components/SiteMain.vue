<template>
  <div class="SiteMain">
      <ListSong :selectedGenre="selectedGenre"/>
  </div>
</template>

<script>
import ListSong from './ListSong.vue'
export default {
  props:["selectedGenre"],
  
    components: {
    ListSong
    },
    data(){
    return{
      response: [],

    }
    },

  
  

    
  
}
</script>

<style lang="scss">
.SiteMain {
    background: #1E2D3B;
    width: 100%;
    height: 1200px;
    
}

</style>
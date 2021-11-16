<template>
  <div class="SiteMain">
      <ListSong :selectedGenre="selectedGenre"/>
  </div>
</template>

<script>
import ListSong from './ListSong.vue'
export default {
    components: {
    ListSong
    },
    data(){
    return{
      selectedGenre: ""
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
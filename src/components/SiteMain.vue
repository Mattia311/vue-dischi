<template>
  <div class="SiteMain">
      <ListSong/>
     
  </div>
</template>

<script>
import ListSong from './ListSong.vue'
export default {
    data () {
        return {
            response: []
        }
    },
    components: {
    ListSong
  }

    

}
</script>

<style lang="scss">
.SiteMain {
    background: #1E2D3B;
    width: 100%;
    height: 1200px;
    
}

</style>
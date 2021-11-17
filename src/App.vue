<template>
  <div id="app">
    <SiteHeader @selectGenres="selectGenres"/>
    <SiteMain :selectedGenre="selectedGenre"/>
    
  </div>
</template>

<script>
import SiteHeader from './components/SiteHeader.vue';
import SiteMain from './components/SiteMain.vue';



export default {
  
  name: 'App',
  components: {
    SiteHeader,
    SiteMain

  },
  data(){
    return{
      selectedGenre: ""
    }
  },
  
  methods:{
    selectGenres(selectedGenre){
    this.selectedGenre = selectedGenre
    }
  }

  
  
}
</script>

<style lang="scss">
@import "../node_modules/bootstrap/scss/bootstrap.scss";

</style>

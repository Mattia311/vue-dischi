<template>
<div class="SiteHeader">
  <div class="row">
      <img src="../assets/Spotify_logo_without_text.svg" alt=""> 
  </div>
  <div>
    <select class="form-select" aria-label="Default select example" v-model="selectGenre"  @change="$emit('selectGenres', selectGenre)">
      <option value= "" selected>Open this select menu to view discs by your favorite genre</option>
      <option value="rock">Rock</option>
      <option value="pop">Pop</option>
      <option value="jazz">Jazz</option>
      <option value="metal">Metal</option>
    </select> 
  </div>
</div>
</template>

<script>
export default {
    data() {
        return {
            selectGenre: ""
        }

    }
     

}
</script>

<style lang="scss">
.SiteHeader {
    background: #2E3A46;
    width: 100%;
    height: 70px;
    display: flex;
    img {
        width: 70px;
        margin-left: 20px;
        margin-top: 2px;
        
    }
    select {
        width: 600px;
        margin-top: 15px;
        margin-left: 400px;
    }

   
}

</style>
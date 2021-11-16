<template>
<div class="SiteHeader">
  <div class="row">
      <img src="../assets/Spotify_logo_without_text.svg" alt=""> 
  </div>
  <div>
    <select class="form-select" aria-label="Default select example">
      <option selected>Open this select menu to view discs by your favorite genre</option>
      <option value="1">Rock</option>
      <option value="2">Pop</option>
      <option value="3">Jazz</option>
      <option value="4">Metal</option>
    </select> 
  </div>
</div>
</template>

<script>
export default {

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
<template>
  <div>
       <div class="d-flex flex-wrap justify-content-center"  >
          <div class="" v-for="(song,index) in filterAlbums" :key="index">
              <div class="respon text-center ">
                  <img  :src="song.poster" alt="">
                  <h3>{{song.title}}</h3>
                  <p>{{song.author}}</p>
                  <p>{{song.year}}</p>
              </div>
          </div>
      </div>
      
  </div>
</template>

<script>
import axios from 'axios';
export default {
    props:["selectedGenre"],
    data () {
        return {
            response: [],
            
        }
    },
    
    mounted () {
        axios
            .get('https://flynn.boolean.careers/exercises/api/array/music')
            .then(r =>{
              console.log(r.data.response);
              this.response = r.data.response
            }).catch(e=>{
              console.log(e, 'ERROR');
            })
          

    },
    computed:{
          filterAlbums(){
            const arrFiltered = this.response.filter(
              (elm) => {
                if(elm.genre.toLowerCase() == this.selectedGenre|| this.selectedGenre == ""){
                  return true
                }
                return false
              }
            )
            return arrFiltered;
          }
        }
     
    
    
    


}
</script>

<style lang="scss">
.d-flex {
        padding-top: 70px;
    }
    .text-center {
        width: 200px;
        background: #2E3A46;
        margin-left:20px;
        margin-right: 20px;
        margin-top: 20px;
        padding-top: 10px;
        height: 370px;
        h3 {
            color: white;
            font-size: 28px;
            margin-bottom: 20px;
            margin-top: 20px;
        }
        p {
            color: #807F7D;
            margin-bottom: 0px;
            
        }
       
    }
    
    img {
        width: 170px;
         
    }

</style>
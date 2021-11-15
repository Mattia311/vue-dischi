<template>
  <div class="SiteMain">
      <div class="row">
          <div class="text-center" v-for="respons in response" :key="respons.poster">
              <div class="respon">
                  <img :src="respons" alt="">
              </div>
          </div>
      </div>
  </div>
</template>

<script>
import axios from 'axios';
export default {
    data () {
        return {
            response: []
        }
    },

    mounted () {
    axios
    .get('https://flynn.boolean.careers/exercises/api/array/music')
    .then(r =>{
      console.log(r.data);
      this.response = r.data
    }).catch(e=>{
      console.log(e, 'ERROR');
    })
  }

}
</script>

<style lang="scss">
.SiteMain {
    background: #1E2D3B;
    width: 100%;
    height: calc(100vh - 70px);
}

</style>
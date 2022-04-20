<template>
  <div class="container mt-3 sfondo_container">
      <div class="cont">
          <DischiComp
            v-for="(element, index) in dischi"
            :key="index"
            :autore='element.author'
            :img='element.poster'
            :anno='element.year'
            :brano='element.title'
          />
      </div>

  </div>
</template>

<script>
import DischiComp from './DischiComp.vue'
import axios from 'axios';

export default {
  name: 'MainComp',
  components:{
      DischiComp
  },
  data() {
      return {
          dischi:[]
      }
  },
  created() {
      axios.get('https://flynn.boolean.careers/exercises/api/array/music')
      .then((res)=>{
          console.log(res.data.response)
          this.dischi=res.data.response
      })
  },

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
    .cont{
        display: flex;
        flex-wrap: wrap;
        
    }
</style>
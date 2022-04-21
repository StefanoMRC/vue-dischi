<template>
<div>
    <HeaderComp @funzRicerca='metodoRicerca'/>
  <div class="container mt-3 sfondo_container ">
      <div class="row row-cols-6">
          <DischiComp           
            v-for="(element, index) in filtraggio"
            :key="index"
            :autore='element.author'
            :img='element.poster'
            :anno='element.year'
            :brano='element.title'
            :genere='element.genre' 
          />
      </div>

  </div>
</div>

</template>

<script>
import HeaderComp from './HeaderComp.vue'
import DischiComp from './DischiComp.vue'
import axios from 'axios';

export default {
  name: 'MainComp',
  components:{
      DischiComp,
      HeaderComp
  },
  data() {
      return {
          dischi:[],
          testoRicerca:''
      }
  },
  computed:{
      filtraggio(){
          if (this.testoRicerca=='') {
              return this.dischi
          }
          return this.dischi.filter((element)=> {
              return element.genre
                    .toLowerCase()
                    .includes(this.testoRicerca.toLowerCase())
          })
      }
  },
  created() {
      axios.get('https://flynn.boolean.careers/exercises/api/array/music')
      .then((res)=>{
          console.log(res.data.response)
          this.dischi=res.data.response
      })
  },
  methods: {
        metodoRicerca(testo){
        this.testoRicerca=testo;
  },
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">

</style>
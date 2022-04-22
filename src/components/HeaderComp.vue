<template>
  <div class="sfondo px-5 py-2 d-flex justify-content-between" >
    <img src="../assets/spotify-logo-png-7053.png" alt="">
    <div class="d-flex flex-column align-item-center">
        <h5>Seleziona un genere:</h5>
        <select class="px-1 text-center" name="" id="" v-model="ricerca" @change.prevent="$emit('funzRicerca', ricerca)">
          <option value="">Tutti i generi</option>
          <option value="Rock">Rock</option>
          <option value="Pop">Pop</option>
          <option value="Jazz">Jazz</option>
          <option value="Metal">Metal</option>
        </select>
    </div>

  </div>
</template>

<script>
export default {
  name: 'HeaderComp',
  data() {
    return {
      ricerca:'',
      
    }
  },
  methods: {

  },
}
</script>


<style scoped lang="scss">
    .sfondo{
        
        background: #2e3a46;
        img{
            height: 50px;
        }
    }
    h5{
      color: white;
    }
</style>
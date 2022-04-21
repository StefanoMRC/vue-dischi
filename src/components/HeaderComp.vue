<template>
  <div class="sfondo px-5 py-2 d-flex justify-content-between" >
    <img src="../assets/spotify-logo-png-7053.png" alt="">
    <select class="px-1 fs-3" name="" id="" v-model="ricerca" @change.prevent="$emit('funzRicerca', ricerca)">
      <option value="Rock">Rock</option>
      <option value="Pop">Pop</option>
      <option value="Jazz">Jazz</option>
      <option value="Metal">Metal</option>
    </select>
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
</style>
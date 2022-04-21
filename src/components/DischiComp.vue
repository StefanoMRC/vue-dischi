<template>
  <div class="text-center col mx-1 my-3 p-3">
    <img :src="img" alt="" class="img-fluid">
    <h4 class="text-uppercase mt-3">{{brano}}</h4>
    <p>{{autore}}</p>
    <span>{{anno}}</span>
  </div>
</template>

<script>
export default {
  name: 'DischiComp',
  props:{
      autore:String,
      img:String,
      anno:String,
      brano:String
  }
}
</script>


<style scoped lang="scss">
    div{
        
        
        background: #2e3a46;
        
        h4{
            color: white;
            margin: 10px 0;
        }
        p{
            margin-bottom: -7px;
            color: #797c7f;
        }
        span{
            color: #797c7f;
        }
    }
</style>

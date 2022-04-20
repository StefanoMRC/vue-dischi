<template>
  <div class="text-center">
    <img :src="img" alt="" class="img-fluid">
    <h3 class="text-uppercase mt-3">{{brano}}</h3>
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
        margin: 15px 15px;
        padding: 10px;
        background: #2e3a46;
        flex-basis: calc((100% / 5) - 40px);
        h3{
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

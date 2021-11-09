<template>
  <div class="bg grey">
  <h1> 一関高専1階</h1>  
  <p class="map1">
  <img src="~/assets/ichinoseki-kosen.jpg">
  </p>
  <ul type="square" class="text" >
    <li>武道館</li>
    <switchArea></switchArea>
    <li>第一体育館</li>
    <switchArea></switchArea>
  </ul>

  </div>
  
</template>

<script>
import switchArea from '~/components/Switch.vue'  
 
export default {

  components: {
    switchArea
  }
}
</script>


<style>
.frex{
  display: flex;
}
p.map1 img{
  width: 500px;
}
.text{
  margin:0 0 0 10px;
  padding:0;
}
</style>>


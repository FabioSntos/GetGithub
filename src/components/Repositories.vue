

<template>
  <div class="repository">
    <h1 class="title">sistema-comentario</h1>
    <p class="description">Descriçao: Experimentações Sistema de comentários usando vue-js</p>
    <span><img src="" alt=""> 0</span>
  </div>
</template>

<script> 
export default {
  name: 'Repositories',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
 .repository{
  font-family: 'Rubik', sans-serif;
  font-weight:300
 }   
  h1 {
    font-size:24px;
  }
  p {
    font-size:16px;
    counter-reset: #757575;
    line-height: 28px;
  }
  span {
    margin-bottom: 25px;
  }
</style>

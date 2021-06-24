<template>
  <Header />
  <Repositories msg="Welcome to Your Vue.js App"/> 
</template>

<script>

import Repositories from './components/Repositories.vue'
import Header from './components/Header.vue'
export default {
  name: 'App',
  components: {
    Header,
    Repositories,
  }
}
</script>

<style>
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
</style>

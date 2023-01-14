<template>
  <div class="home">
    <link rel="stylesheet" 
        href="https://use.fontawesome.com/releases/v5.2.0/css/all.css" 
        integrity="sha384-hWVjflwFxL6sNzntih27bfxkr27PmbbK/iSvJ+a4+0owXq79v+lsFkW54bOGbiDQ" 
        crossorigin="anonymous">
     <Header />   
    <Categories/>
    <Principal />
  
  </div>
</template>

<script>
// @ is an alias to /src
import Search from '@/components/Header/Search.vue'
import Principal from '@/components/Home/Principal.vue'
import Categories from '@/components/Home/Categories.vue'
import Header from '@/components/Header.vue'

export default {
  name: 'HomeView',
  components: {
    Principal, Categories, Header, Search
  }
}
</script>
<style>
.home{
  display: flex;
  flex-flow:  wrap row;
  align-items:flex-start;
  justify-content: space-evenly;


}
</style>
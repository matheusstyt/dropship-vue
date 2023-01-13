<template>
  <div class="home">
    <link rel="stylesheet" 
        href="https://use.fontawesome.com/releases/v5.2.0/css/all.css" 
        integrity="sha384-hWVjflwFxL6sNzntih27bfxkr27PmbbK/iSvJ+a4+0owXq79v+lsFkW54bOGbiDQ" 
        crossorigin="anonymous">
        
    <Categories/>
    <Principal />
  
  </div>
</template>

<script>
// @ is an alias to /src
import Principal from '@/components/Principal.vue'
import Categories from '@/components/Categories.vue'
import { FontAwesomeIcon } from "@fortawesome/vue-fontawesome";
import { library } from "@fortawesome/fontawesome-svg-core";
import { faPhone } from "@fortawesome/free-solid-svg-icons";
library.add(faPhone);
export default {
  name: 'HomeView',
  components: {
    Principal, Categories, FontAwesomeIcon
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
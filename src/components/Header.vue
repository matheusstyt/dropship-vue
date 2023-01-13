<template>
    <header>
        <div class="img-content">
            <img id="logo" src="../assets/tools/logo.png" alt="logo">
        </div>
        <Search />
        <Profile />
     
    </header>
</template>
<script>
import Search from './Search.vue'
import Profile from './Profile.vue'
export default {
    components:{
        Search, Profile
    }
    
}
</script>
<style lang="scss">
header{
    display: flex;
    justify-content: center;
    align-items: center;
    flex-flow: row;
    margin-bottom: 1em;
    padding: 1vmax;
    background-color: rgb(241, 241, 241);
    width: 100%;
    height: 60px;
}
.img-content{
    height: 100%;
    aspect-ratio: 50/10;
    #logo{
        height: 100%;
        width: 100%;
    }
}

</style>
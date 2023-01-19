<template>
    <header>
        <div class="img-content">
            <img id="logo" @click="getHome()" src="@/assets/tools/logo.png" alt="logo">  
        </div>
        <Search />
        <Profile />
     
    </header>
</template>
<script>
import Search from './Header/Search.vue'
import Profile from './Header/Profile.vue'
export default {
    components:{
        Search, Profile
    },
    methods:{
        getHome(){
            window.location.href = '/';
        }
    }
    
}
</script>
<style lang="scss" scoped>
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
header:hover{
    background-color: rgb(234, 234, 236);
}
.img-content{
    height: 100%;
    aspect-ratio: 50/10;
    #logo{
        height: 100%;
        width: 100%;
        cursor: pointer;
    }
}

</style>
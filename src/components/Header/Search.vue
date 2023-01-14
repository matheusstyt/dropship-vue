<template>
    <div class="search-container">
        <input type="search" name="search" id="search">
        <div class="glass-content">
            <img src="@/assets/tools/search-icon.svg" alt="">
        </div>
        
    </div>
</template>
<style lang="scss">
.search-container{
    width: 95%;
    height: 40px;
    overflow: hidden;
    display: flex;
    flex-flow: row;
   // justify-content: space-between;
    
    border: 0px solid rgb(88, 115, 238);
    border-radius: 0px;
    #search[type="search"]{
        width: 100%;
        border: 2px solid rgb(88, 115, 238);
        font-size: 14px;
        font-family: 'Arial';
        padding: 0.5em 1em;
    }
    #search[type="search"]:active{
        border-color: aqua;
    }
    .glass-content{
        background-color: rgb(101, 120, 228);
        margin-right: -1px;
        height: 100%;
        aspect-ratio: 1/1;
        
        display: flex;
        align-items: center;
        justify-content: center;
        img{
            height: 45%;
            aspect-ratio: 1/1;

        }
    }
}

</style>
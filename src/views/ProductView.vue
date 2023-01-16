<template>
    <div>
        <Header/>
        <main class="container-product">
            <section class="img-product">
                <img class="main-photo" :src="mainImg" alt="">
                <ul class="list-photo">
                    <li @mouseover="firstImg = true" @mouseleave="firstImg = false"><img :src="dataImg[0].src" alt=""></li>
                    <li @mouseover="secondImg = true" @mouseleave="secondImg = false"><img :src="dataImg[1].src" alt=""></li>
                    <li @mouseover="thirdImg = true" @mouseleave="thirdImg = false"><img :src="dataImg[2].src" alt=""></li>
                    <li @mouseover="fourthImg = true" @mouseleave="fourthImg = false"><img :src="dataImg[3].src" alt=""></li>
                    <li @mouseover="packImg = true" @mouseleave="packImg = false"><p>+3</p></li>
                    <!-- <li><img src="https://i.ebayimg.com/images/g/atkAAOSwMl1japLw/s-l1600.png" alt=""></li>
                    <li><img src="https://i.ebayimg.com/images/g/aBIAAOSwHEljapJ~/s-l1600.jpg" alt=""></li>
                    <li><img src="https://i.ebayimg.com/images/g/bgEAAOSwhCxjapKA/s-l1600.jpg" alt=""></li>
                    <li><img src="https://i.ebayimg.com/images/g/VGIAAOSws7ljapKB/s-l1600.jpg" alt=""></li>
                    <li><img src="https://i.ebayimg.com/images/g/5I8AAOSwZk5japKD/s-l1600.jpg" alt=""></li> -->

                </ul>
            </section>
            <section class="details-product">
                <h1>Produto 1</h1>

            </section>
            
        </main>

    </div>
    
</template>
<script>
import Header from '@/components/Header.vue'
export default {
    components: {
        Header
  },
    data(){
        return{
            data: null,
            dataImg: [
                {id:1, src:"https://i.ebayimg.com/images/g/eBMAAOSwcmRjaprI/s-l1600.png"},
                {id:2, src:"https://i.ebayimg.com/images/g/h8oAAOSw5b5japKA/s-l1600.jpg"},
                {id:3, src:"https://i.ebayimg.com/images/g/RWoAAOSw1HxjapKB/s-l1600.jpg"},
                {id:4, src:"https://i.ebayimg.com/images/g/SdAAAOSw1ExjapL~/s-l1600.png"},
                {id:5, src:"https://i.ebayimg.com/images/g/atkAAOSwMl1japLw/s-l1600.png"},
                {id:6, src:"https://i.ebayimg.com/images/g/atkAAOSwMl1japLw/s-l1600.png"},
                {id:7, src:"https://i.ebayimg.com/images/g/bgEAAOSwhCxjapKA/s-l1600.jpg"},
                {id:8, src:"https://i.ebayimg.com/images/g/bgEAAOSwhCxjapKA/s-l1600.jpg"},
                {id:9, src:"https://i.ebayimg.com/images/g/VGIAAOSws7ljapKB/s-l1600.jpg"},
                {id:10, src:"https://i.ebayimg.com/images/g/5I8AAOSwZk5japKD/s-l1600.jpg"},

            ],
            firstImg: true,
            secondImg: false,
            thirdImg: false,
            fourthImg: false,
            packImg: false,
            mainImg: null

        }
    },
    watch:{
        firstImg(newValue){ 
            if(newValue){
                this.mainImg = this.dataImg[1].src
            }
            console.log('fisrt'+newValue); 
    },
        secondImg(newValue){ 
            if(newValue){
                this.mainImg = this.dataImg[2].src
            }
            console.log('second'+newValue); 
    },
        thirdImg(newValue){ 
            if(newValue){
                this.mainImg = this.dataImg[3].src
            }
            console.log('third'+newValue); 
    },
        fourthImg(newValue){ 
            
            console.log('fourth'+newValue); 
    },
        packImg(newValue){ 
            
            console.log('pack'+newValue); 
    },
    },
    created(){
        this.mainImg = this.dataImg[0].src
     // this.data = this.$router.params.data
        console.log(this.data);
    }
}
</script>
<style lang="scss" scoped>
main{
    max-width: 100%;
    width: 100%;
}
.container-product{
    display: flex;
    background-color: bisque;
    width: 100%;
}
.img-product{
    display: flex;
    flex-flow: row wrap;
    width: 45%;
    background-color: rgba(0, 0, 0,0.3);
}
.details-product{
    width: 55%;
    background-color: rgba(0, 0, 0,0.5);
}
.main-photo{
    width: 75%;
    aspect-ratio: 4/3;
}
.list-photo{
    width: 10%;
    list-style-type: none;

    li{
        overflow: hidden;
    }
    li img{
        width: 100%;
        aspect-ratio: 1/1;
    }
    li p{
        width: 100%;
        aspect-ratio: 1/1;
        background-color: aliceblue;
        display: flex;
        align-items: center;
        justify-content: center;
    }
}
</style>
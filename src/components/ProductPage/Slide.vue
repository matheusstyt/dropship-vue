<template>
    <section class="img-product">
        <img class="main-photo" :src="mainImg" alt="">
        <ul class="list-photo">
            <li @mouseover="firstImg = true" @mouseleave="firstImg = false"><img id="img1" crossorigin="anonymous" :src="dataImg[0].src" alt=""></li>
            <li @mouseover="secondImg = true" @mouseleave="secondImg = false"><img id="img2" crossorigin="anonymous" :src="dataImg[1].src" alt=""></li>
            <li @mouseover="thirdImg = true" @mouseleave="thirdImg = false"><img id="img3" crossorigin="anonymous" :src="dataImg[2].src" alt=""></li>
            <li @mouseover="fourthImg = true" @mouseleave="fourthImg = false"><img id="img4" crossorigin="anonymous" :src="dataImg[3].src" alt=""></li>
            <li @mouseover="packImg = true" @mouseleave="packImg = false"><strong><span>+3</span></strong></li>
            <!-- <li><img src="https://i.ebayimg.com/images/g/atkAAOSwMl1japLw/s-l1600.png" alt=""></li>
            <li><img src="https://i.ebayimg.com/images/g/aBIAAOSwHEljapJ~/s-l1600.jpg" alt=""></li>
            <li><img src="https://i.ebayimg.com/images/g/bgEAAOSwhCxjapKA/s-l1600.jpg" alt=""></li>
            <li><img src="https://i.ebayimg.com/images/g/VGIAAOSws7ljapKB/s-l1600.jpg" alt=""></li>
            <li><img src="https://i.ebayimg.com/images/g/5I8AAOSwZk5japKD/s-l1600.jpg" alt=""></li> -->
        </ul>
    </section>

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
    methods:{
        changeOpacity(img){
            if(img === 0){
                document.getElementById('img1').style.opacity = 1;
                document.getElementById('img2').style.opacity = 0.6;
                document.getElementById('img3').style.opacity = 0.6;
                document.getElementById('img4').style.opacity = 0.6;
            }else if(img === 1){
                document.getElementById('img1').style.opacity = 0.6;
                document.getElementById('img2').style.opacity = 1;
                document.getElementById('img3').style.opacity = 0.6;
                document.getElementById('img4').style.opacity = 0.6;
            }else if(img === 2){
                document.getElementById('img1').style.opacity = 0.6;
                document.getElementById('img2').style.opacity = 0.6;
                document.getElementById('img3').style.opacity = 1;
                document.getElementById('img4').style.opacity = 0.6;
            }else if(img === 3){
                document.getElementById('img1').style.opacity = 0.6;
                document.getElementById('img2').style.opacity = 0.6;
                document.getElementById('img3').style.opacity = 0.6;
                document.getElementById('img4').style.opacity = 1;
            }
        }
    },
    watch:{
        firstImg(newValue){ 
            if(newValue){
                this.mainImg = this.dataImg[0].src
                this.changeOpacity(0);
            }
    },
        secondImg(newValue){ 
            if(newValue){
                this.mainImg = this.dataImg[1].src
                this.changeOpacity(1);
            }
    },
        thirdImg(newValue){ 
            if(newValue){
                this.mainImg = this.dataImg[2].src
                this.changeOpacity(2);
            }
    },
        fourthImg(newValue){ 
            if(newValue){
                this.mainImg = this.dataImg[3].src
                this.changeOpacity(3);
            }
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
.img-product{
    display: flex;
    flex-flow: row wrap;
    gap: 1em;
    width: 45%;

    aspect-ratio: 4/3;
   // background-color: rgba(0, 0, 0,0.3);
}

.main-photo{
    width: 82%;
    aspect-ratio: 1/1;
    max-height: 100%;
    cursor: pointer;
    border: 1px solid rgba(0, 0, 0, 0.3);
    overflow: hidden;
}
.list-photo{
    width: 14%;
    margin: 0;
    padding: 0;
    list-style-type: none;
    display: flex;
    flex-flow: row wrap;
    gap: 1em;
    //overflow-y: scroll;
    height: 100%;
    border-bottom: 5px solid hsla(0,0%,100%,.5);
    li{
        overflow: hidden;
        aspect-ratio: 1/1;
    }
    li:first-child{
        background-color: transparent;
    }
    li img{
        width: 90%;
        aspect-ratio: 1/1;
        opacity: 0.7;
        //cursor: pointer;
        //border: 1px solid rgba(0, 0, 0, 0.3);
        //overflow: hidden;
    }
    li img:hover{
        transition: ease 0.2s;
        opacity: 1;
        .main-photo{
            src: v-bind('mainImg[2].src');
        }
    }
    li{
        width: 90%;
        aspect-ratio: 1/1;
        display: flex;
        align-items: center;
        justify-content: center;
        cursor: pointer;
        border: 1px solid rgba(0, 0, 0, 0.3);
    }
    li strong{
        display: flex;
        align-items: center;
        justify-content: center;
        width: 100%;
        height: 100%;
    }
    li strong:hover{
        transition: ease 0.2s;
        background-color: rgba(0, 0, 0, 0.1);
        
    }
}
</style>
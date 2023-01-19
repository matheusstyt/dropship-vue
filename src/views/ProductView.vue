<template>
    <div>
        <Header/>
        <main class="container-product">
            <Slide/>
            <section class="details-product">
                <h1>{{product_name}}</h1>
                <div class="evaculation-content-flex">
                    <div class="evaculation-icon-content">&#9733;&#9733;&#9733;&#9733;&#9733;<strong class="evaculation-median-content">{{average}}</strong></div>
                    <p class="evaculation-text-content">{{product_average}} avaliações</p>
                    <p class="sold-text-content">{{product_sold}} pedidos</p>
                </div>
                <hr>
                <section class="price-container">
                    <h3>R$ {{product_price_n}}</h3>
                    <h3 class="price-desc">R$ {{product_price_des}}</h3>
                    <div class="paymment-options-container">
                        <h4>Opções de pagamentos disponíveis:</h4>
                        <div class="paymment-options">
                            <img src="@/assets/bags-paymment/pix-icon.svg" alt="">
                            <img src="@/assets/bags-paymment/boleto-icon.svg" alt="">
                            <img src="@/assets/bags-paymment/visa-icon.png" alt="">
                            <img src="@/assets/bags-paymment/mc-icon.svg" alt="">
                            <img src="@/assets/bags-paymment/elo-icon.png" alt="">
                            <img src="@/assets/bags-paymment/amex-icon.svg" alt="">

                        </div>
                    </div>
                    
                </section>
                <section class="ships-container">
                    <h3>Frete Grátis</h3>
                    <p>Origem : {{product_origin}} </p>
                    <p>Destino : {{product_destiny}}</p>
                    <p>Via : {{product_shipping}}</p>
                </section>
                <section class="buy-container">
                    <button>Ir á página de compras</button>
                    <svg class="heart-icon" @click="setlike()" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 959.41 880.1">
                        <path id="heart" d="M479.71,137.75C399.76-79.31,0-45.73,0,280.47c0,162.7,122.33,379,479.71,599.63,357.38-220.66,479.7-436.93,479.7-599.63C959.41-43.73,559.66-79.31,479.71,137.75Z" fill="#ed1c24"/></svg>
                    <!-- <p id="like-set" @click="setlike()" @mouseover="firstImg = true" @mouseleave="firstImg" >&#9825;</p> -->
                </section>
            </section>
            
        </main>
        <About/>
        <Evaculation  :totalAverage="totalAverage" :product_evaculation="product_evaculation" :product_average="product_average"/>
    </div>
    
</template>
<script>
import Header from '@/components/Header.vue'
import Slide from '@/components/ProductPage/Slide.vue'
import About from '@/components/ProductPage/About.vue'
import Evaculation from '@/components/ProductPage/Evaculation.vue' 
export default {
    components: {
        Header, Slide, About, Evaculation
  },
    data(){
        return{
            data: null,
            liked: false,
            product_name: 'Microsoft Xbox Series X 1TB Video Game Console - Black',
            product_price_n: '3.214,88',
            product_price_des: '4.314,88',   
            product_origin: 'China',
            product_destiny: 'Brazil',
            product_shipping: 'AliExpress Standard Shipping',
            product_sold: '467',
            product_average: 0,
            product_evaculation : 0,
            totalAverage:[
                {value: 1, average: 45, percent: 0},
                {value: 2, average: 1, percent: 0},
                {value: 3, average: 21, percent: 0},
                {value: 4, average: 80, percent: 0},
                {value: 5, average: 1997, percent: 0}
            ]
        }
    },
    methods:{
        averageFunction(){
            let x = 0;
            let p = 0;
            this.totalAverage.forEach(element => {
                x = x + element.value*element.average;
                p = p + element.average;
                element.percent = element.average
            });
            this.product_average = p;
             this.totalAverage.forEach(element => {
                var x = (element.average/p)*100
                element.percent = x.toFixed(1);
            });
            let average = x/p;
            this.product_evaculation = average.toFixed(1);
        },
        setlike(){
            if(this.liked){
                document.getElementById('heart').style.fill = 'rgb(138, 138, 138)';
                this.liked = !this.liked;
            }else{
                document.getElementById('heart').style.fill = 'rgb(238, 96, 96)';
                this.liked = !this.liked;
            }
        }
    },
    created(){
        this.averageFunction();
    }

}
</script>
<style lang="scss">
body{ 
    background-color: #fff;
}
$color_heart :  rgb(138, 138, 138);
$color_heart_hover : rgb(43, 43, 43);
$color_heart_active : rgb(165, 50, 50);
@mixin reset(){
    padding: 0;
    margin: 0;
}
@mixin flex(){
    display: flex;
}
main{
    
    max-width: 100%;
    background-color: aqua;
    
}
h1{
    text-align: left;
    margin: 0;
}
.evaculation-content-flex{
    display: flex;
    justify-content: flex-start;
    align-items: flex-end;
    gap: 1em;
    .evaculation-icon-content{
        @include reset();
        color: rgb(16, 85, 211);
        strong{
            color:rgb(90, 90, 90);
            padding: 0 0.3em;
        }
    }
    .evaculation-text-content, .evaculation-median-content, .sold-text-content{
        @include reset();
    }

}
.container-product{
    display: flex;
    background-color: white;
    width: 97%;
    @include reset();
}
.details-product{
    width: 50%;
    padding: 0 2em;
    //background-color: rgba(0, 0, 0,0.5);
}
.price-container{
    h3{
        font-size: 3em;
        text-align: left;

    }
    .price-desc{
        text-decoration:line-through;
        color: rgba(241, 2, 2, 0.459);
        font-size: 2em;
    }
}
.paymment-options{
    padding: 0.5em 0.3em;
    border: 1px solid rgba(0,0,0,0.2);
    border-radius: 10px;
    display: flex;
    flex-flow: row wrap;
    justify-content: space-around;
    p{
        background-color: antiquewhite;
    }
    img{
        height: 90px;
       
    }
}
.ships-container{
    margin-top: 1em;
    text-align: left;
}
.buy-container{
    text-align: left;
    margin-top: 1em;
    display: flex;
    justify-content: space-evenly;
    button{
        background-color: rgb(88, 115, 238);
        color: #fff;
        border-radius: 3px;
        font-size: 1.2em;
        padding: 0.3em;
        font-family: 'Arial';
        border: 2px solid rgba(0,0,0, 0.3);
        
    }
    button:hover{
        background-color: rgb(70, 98, 224);
        box-shadow: 0px 0px 10px rgb(0 0 0 / 0.4);  
    }
    button:active{
        background-color: rgb(34, 64, 199);
        box-shadow: 0px 0px 10px rgb(0 0 0 / 0.4);  
    }
    p{
        font-size: 3em;
        @include reset();
    }
    .heart-icon{
        width: 2em;
        path{
            fill: $color_heart;     
        }
    }
    .heart-icon:hover{
        filter: drop-shadow(0px 0px 4px rgb(0 0 0 / 0.4));  
        transition: ease 0.1s;
    }
    .heart-icon:active{
        transform: scale(1.4);
        transition: all 0.1s linear;
    }

}
</style>
<template>
    <div>
        <Header/>
        <main class="container-product">
            <Slide/>
            <section class="details-product">
                <h1>Microsoft Xbox Series X 1TB Video Game Console - Black</h1>
                <div class="evaculation-content-flex">
                    <div class="evaculation-icon-content">&#9733;&#9733;&#9733;&#9733;&#9733;<strong class="evaculation-median-content">5.0</strong></div>
                    <p class="evaculation-text-content">152 avaliações</p>
                    <p class="sold-text-content">467 pedidos</p>
                </div>
                <hr>
                <section class="price-container">
                    <h3>R$ 3.214,88</h3>
                    <h3 class="price-desc">R$ 4.314,88</h3>
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
                    <p>Origem : China </p>
                    <p>Destino : Brasil</p>
                    <p>Via : AliExpress Standard Shipping</p>
                </section>
                <section class="buy-container">
                    <button>Ir á página de compras</button>
                    <p id="like-set" @click="setlike()" @mouseover="firstImg = true" @mouseleave="firstImg" >&#9825;</p>
                </section>
            </section>
            
        </main>

    </div>
    
</template>
<script>
import Header from '@/components/Header.vue'
import Slide from '@/components/ProductPage/Slide.vue'
import { decode } from 'punycode';
export default {
    components: {
        Header, Slide
  },
    data(){
        return{
            data: null,
            heart: ''
        }
    },
    methods:{
        setlike(){
            document.getElementById('like-set').textContent =  decode(&#10084);
        }
    }

}
</script>
<style lang="scss" scoped>
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
        padding: 0;
        margin: 0;
        color: rgb(16, 85, 211);
        strong{
            color:rgb(90, 90, 90);
            padding: 0 0.3em;
        }
    }
    .evaculation-text-content, .evaculation-median-content, .sold-text-content{
        padding: 0;
        margin: 0;
    }

}
.container-product{
    display: flex;
    background-color: white;
    width: 97%;
    margin: 0 auto;
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
        background-color: rgb(243, 243, 243);
        border-radius: 5px;
        font-size: 1.2em;
        padding: 0.3em;
        font-family: 'Arial';
    }
    button:hover{
        background-color: rgb(218, 232, 245);
    }
    p{
        font-size: 3em;
        margin: 0;
        padding: 0;
    }

}
</style>
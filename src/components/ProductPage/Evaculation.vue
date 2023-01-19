<template>
    <section class="block-evaculation">
        <h2>Avaliações</h2>
        <hr>
        <div class="flex">
            <div class="evaculation-median-container">
                <strong id="value-median"><span>{{product_evaculation}}</span></strong>
                <div class="icon-content flex">
                    <p>&#9733;</p>
                    <p>&#9733;</p>
                    <p>&#9733;</p>
                    <p>&#9733;</p>
                    <p>&#9733;</p>
                </div>
                <p id="total-evaculation">{{product_average}} avaliações do produto</p>
            </div>
            <div  class="bar-evaculation-container">
                <div v-for="(index) in totalAverage" id="bar-line" class="flex">
                    <svg height="1.4em" width="1.4em" version="1.1" id="Capa_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" 
                            viewBox="0 0 47.94 47.94" xml:space="preserve">
                        <path style="fill: rgb(173, 186, 201)" d="M26.285,2.486l5.407,10.956c0.376,0.762,1.103,1.29,1.944,1.412l12.091,1.757
                            c2.118,0.308,2.963,2.91,1.431,4.403l-8.749,8.528c-0.608,0.593-0.886,1.448-0.742,2.285l2.065,12.042
                            c0.362,2.109-1.852,3.717-3.746,2.722l-10.814-5.685c-0.752-0.395-1.651-0.395-2.403,0l-10.814,5.685
                            c-1.894,0.996-4.108-0.613-3.746-2.722l2.065-12.042c0.144-0.837-0.134-1.692-0.742-2.285l-8.749-8.528
                            c-1.532-1.494-0.687-4.096,1.431-4.403l12.091-1.757c0.841-0.122,1.568-0.65,1.944-1.412l5.407-10.956
                            C22.602,0.567,25.338,0.567,26.285,2.486z"/>
                    </svg>
                    <p id="bar-number">{{index.value}}</p>
                    <div class="bar-content">
                        <p id="text-percent">{{index.percent}}%</p>
                        <div id="bar-width" :style="{ width : index.percent+'%'}"></div>
                    </div>
                    <p id="total-line">{{index.average}}</p>
                </div>
            </div>
        </div>
        
    </section>
</template>
<script>
export default {
    props:{
        totalAverage : Object,
        product_average : Number,
        product_evaculation : Number

    },
    data(){
        return{

        }
    },
    created(){

    },
    methods:{

    }
}
</script>
<style lang="scss" scoped>


.block-evaculation{
    border: 1px solid rgba(0,0,0 ,0.4);
    border-radius: 10px;
    padding: 1em;
    width: 90%;
    margin: 2em auto;
}
    h2, p, strong, span{
        text-align: left;
        margin: 0;
        padding: 0%;
    }
    .flex{
        display: flex;
        
    }
    .evaculation-median-container{
        padding: 0 1.5em;
        strong{
            font-size: 5em;
        }
        .icon-content{
            font-size: 2.3em;
            justify-content: center;
        }
        .total-evaculation{
            font-size: 0.8em;

        }
    }
    .bar-evaculation-container{
        width: 30%;
        margin-top: 1em;
        #bar-line{
            align-items: center;
            justify-content: flex-start;
            height: 1.5em;
            gap: 0.3em;
            margin-bottom: 0.5em;
            .star-svg{
                path{
                    fill: rgb(173, 186, 201)
                }
                
            }
            .bar-content{
                border-radius: 15px;
                overflow: hidden;
                position: relative;
                background-color: rgb(176, 189, 192);
                width: 70%;
                height: 100%;
                #text-percent{
                    color: #fff;
                    position: absolute;
                    text-shadow: 1px 1px 1px black;
                    top: 10%;
                    left: 45%;
                    
                }
                #bar-width{
                    background-color: rgb(74, 121, 192);
                    width: 87%;
                    height: 100%;
                }
            }
        }
    }
    
</style>
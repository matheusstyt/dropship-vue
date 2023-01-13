<template>
<main>
    <div v-for="(index) in products" key="index" class="item">
        <div class="photo">
            <img :src="index.url">
        </div>
        <div class="flex-price">
            <h4>R$</h4><h2>{{index.price}}</h2><h4>,07</h4>
        </div>
        <p>{{index.sold}} vendidos</p>
        <P>{{index.description}}</P>
        <div class="evaluation-content">
            <div class="favorites-start">
                <div class="stars-content">
                    <h4 id="evaluationIcon">&#9733;&#9733;&#9733;&#9733;&#9734;</h4>
                     <p id="evaluationNumber">{{index.evaluation}}</p>
                </div>
                
                <div class="likes-content">
                    <h4 id="likes-icon">&#10084;</h4>
                    <h4 id="likes-count">{{index.likes}}</h4>  
                </div>
            </div>
           
        </div>
    </div>
  
    
</main>
</template>
<script>
export default {
    data(){
        return{
            products :[
                {url: "https://www.petz.com.br/blog/wp-content/uploads/2019/07/vida-de-gato.jpg", price:"40,50", sold:"57", description: "Descrição do produto 1", evaluation:"5", likes:"25" },
                {url: "https://itpetblog.com.br/wp-content/uploads/2021/04/poderes-magicos-gatos.jpg", price:"490,50", sold:"232", description: "Descrição do produto 2", evaluation:"2", likes:"40" },
                {url: "https://midias.agazeta.com.br/2021/04/12/produtos-para-gatos-472152-article.png", price:"700,00", sold:"100", description: "Descrição do produto 3", evaluation:"4.6", likes:"140" },
                {url: "https://www.azpetshop.com.br/blog/wp-content/uploads/2021/03/quantos-anos-vive-um-gato.jpg", price:"240,60", sold:"68", description: "Descrição  do produto 4", evaluation:"3.7", likes:"45" },
                {url: "https://www.petz.com.br/blog/wp-content/uploads/2019/07/vida-de-gato.jpg", price:"40,50", sold:"57", description: "Descrição do produto 1", evaluation:"5", likes:"25" },
                {url: "https://itpetblog.com.br/wp-content/uploads/2021/04/poderes-magicos-gatos.jpg", price:"490,50", sold:"232", description: "Descrição do produto 2", evaluation:"2", likes:"40" },
                {url: "https://midias.agazeta.com.br/2021/04/12/produtos-para-gatos-472152-article.png", price:"700,00", sold:"100", description: "Descrição do produto 3", evaluation:"4.6", likes:"140" },
                {url: "https://www.azpetshop.com.br/blog/wp-content/uploads/2021/03/quantos-anos-vive-um-gato.jpg", price:"240,60", sold:"68", description: "Descrição  do produto 4", evaluation:"3.7", likes:"45" },
                {url: "https://www.petz.com.br/blog/wp-content/uploads/2019/07/vida-de-gato.jpg", price:"40,50", sold:"57", description: "Descrição do produto 1", evaluation:"5", likes:"25" },
                {url: "https://itpetblog.com.br/wp-content/uploads/2021/04/poderes-magicos-gatos.jpg", price:"490,50", sold:"232", description: "Descrição do produto 2", evaluation:"2", likes:"40" },
                {url: "https://midias.agazeta.com.br/2021/04/12/produtos-para-gatos-472152-article.png", price:"700,00", sold:"100", description: "Descrição do produto 3", evaluation:"4.6", likes:"140" },
                {url: "https://www.azpetshop.com.br/blog/wp-content/uploads/2021/03/quantos-anos-vive-um-gato.jpg", price:"240,60", sold:"68", description: "Descrição  do produto 4", evaluation:"3.7", likes:"45" },
                {url: "https://www.petz.com.br/blog/wp-content/uploads/2019/07/vida-de-gato.jpg", price:"40,50", sold:"57", description: "Descrição do produto 1", evaluation:"5", likes:"25" },
                {url: "https://itpetblog.com.br/wp-content/uploads/2021/04/poderes-magicos-gatos.jpg", price:"490,50", sold:"232", description: "Descrição do produto 2", evaluation:"2", likes:"40" },
                {url: "https://midias.agazeta.com.br/2021/04/12/produtos-para-gatos-472152-article.png", price:"700,00", sold:"100", description: "Descrição do produto 3", evaluation:"4.6", likes:"140" },
                {url: "https://www.azpetshop.com.br/blog/wp-content/uploads/2021/03/quantos-anos-vive-um-gato.jpg", price:"240,60", sold:"68", description: "Descrição  do produto 4", evaluation:"3.7", likes:"45" },
            ]
        }
    }
}
</script>
<style lang="scss">
h6, h4, h2, p{
    color: rgb(65, 65, 65);
    margin: 0;
    padding: 0;
}
p{
    text-align: left;
    padding: 0.2em 0.5em;
}
main{
    display: flex;
    flex-flow: row wrap;
    gap: 0.7vmax;
    background-color: rgba(0,0,0, 0.0);
    justify-content: center;
    align-items: flex-start;
    min-width: 17%;
    max-width: 75%;
    width: auto;

}
.item{
    width: 230px;
    height: 360px;
    border-radius: 0.6em;
    background-color: rgb(231, 231, 231);
    overflow: hidden;
}
.item .photo{
    width: 100%;
    aspect-ratio: 1/1;
    //background-image: url(../assets/px200.png);
    background-repeat: no-repeat;
    background-position: center;
    background-size: contain;
    margin-bottom: 1em;
    img{
        width: 100%;
        aspect-ratio: 1/1;
    }
}
.flex-price{
    padding: 0 0.5em;
    display: flex;
    justify-content:flex-start;
    align-items: flex-end;
    
}
.flex-price h2, .flex-price h4{
    color: rgb(165, 25, 25);
}


.item:hover{    
    box-shadow: 0 0 10px rgba(0,0,0, 0.3);
    transition: ease 0.2s;
    .flex-price h2, .flex-price h4{
        color: rgb(211, 29, 29);
    }
    #evaluationIcon{
        color: rgb(16, 85, 211);
    }
}
.favorites-start{
    display: flex;
    align-items: center;
    justify-content: space-evenly;
    h4{
        color: rgb(212, 55, 69);
    }
}
.stars-content{
    display: flex;
    #evaluationIcon, p{
        color: rgb(26, 82, 167);
    }
   
}
.likes-content{
    display: flex;
    align-items:center;
    flex-flow: row;
    justify-content: space-between;

}
</style>
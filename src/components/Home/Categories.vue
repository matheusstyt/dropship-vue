<template>
    <aside class="categories-container">
        <div class="categories-title-content">
            <svg class="categories-css" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 400 512" width="16" height="16" ><!--! Font Awesome Pro 6.2.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. --><path d="M0 96C0 78.3 14.3 64 32 64H416c17.7 0 32 14.3 32 32s-14.3 32-32 32H32C14.3 128 0 113.7 0 96zM0 256c0-17.7 14.3-32 32-32H416c17.7 0 32 14.3 32 32s-14.3 32-32 32H32c-17.7 0-32-14.3-32-32zM448 416c0 17.7-14.3 32-32 32H32c-17.7 0-32-14.3-32-32s14.3-32 32-32H416c17.7 0 32 14.3 32 32z"/></svg>
            <h3>Categorias</h3>
        </div>
        
        <div class="item-category" v-for="item in categories" :key="id">
            <img class="item-css-icon" :src="item.src" alt="">
            <p>{{item.name}}</p>
        </div>
 

    </aside>

</template>
<script>
export default {
    data() {
        return {
            color :"blue",
            categories: [
                {id: 1, name : 'Telefonia e Celulares', src: "@/assets/categories-icons/smartphone-icon.svg"},
                {id: 2, name : 'Laptops e Computadores', src: "@/assets/categories-icons/laptop-icon.svg"},
                {id: 3, name : 'Automóveis', src: "@/assets/categories-icons/smartphone-icon.svg"},
                {id: 4, name : 'Eletrônicos', src: "@/assets/categories-icons/game-icon.svg"},
                {id: 5, name : 'Brinquedos e acessórios infantis', src: "@/assets/categories-icons/toys-icon.svg"},
                {id: 6, name : 'Ferramentas e Untecílios', src: "@/assets/categories-icons/tools-icon.svg"},
                {id: 7, name : 'Relógios e Joias', src: "@/assets/categories-icons/watch-icon.svg"},
                {id: 8, name : 'Esportes e Fitness', src: "@/assets/categories-icons/skipping-icon.svg"},
                {id: 9, name : 'Indústria e Comércios', src: "@/assets/categories-icons/manage-icon.svg"},
                {id: 10, name : 'Eletrodomésticos', src: "@/assets/categories-icons/fan-icon.svg"},
                {id: 11, name : 'Construção Civil', src: "@/assets/categories-icons/brick-icon.svg"},
                {id: 12, name : 'Casa e Lazer', src: "@/assets/categories-icons/house-icon.svg"},
                {id: 13, name : 'Calçados', src: "@/assets/categories-icons/shoes-icon.svg"},
                {id: 14, name : 'Perfumes', src: "@/assets/categories-icons/fragrance-icon.svg"},
            ]
        }
    },
}
</script>
<style lang="scss">
h3{
    margin: 0;
}
aside{
    background-color: #fff;
}
aside:hover{
    box-shadow: 0px 5px 5px rgba(0, 0, 0, 0.1);
    transition: ease 1s;

    .categories-css{
        fill: rgb(33, 101, 204);
    }
}
.categories-title-content{
    display: flex;
    flex-flow: row ;
    align-items: center;
    justify-content: flex-start;
    gap: 0.5em;
    padding: 1em;

}
.item-category:nth-child(2n){
    background-color: rgb(243, 243, 243);
}
.item-category{
    padding: 0.5em 1em;
    display: flex;
    justify-content: flex-start;
    align-items: center;
    cursor: pointer;
}
.item-category:hover{
    background-color: rgba(141, 141, 141, 0.1);
    transition: ease 0.1s;
    .item-css-icon{
        color: rgb(33, 101, 204);
    }
    p{
        color: rgb(33, 101, 204);
    }
}

.item-css-icon{
    width: 14px;
}
</style>
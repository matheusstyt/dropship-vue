<template>
    <aside class="categories-container">
        <div class="categories-title-content">
            <svg class="categories-css" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 400 512" width="16" height="16" ><!--! Font Awesome Pro 6.2.1 by @fontawesome - https://fontawesome.com License - https://fontawesome.com/license (Commercial License) Copyright 2022 Fonticons, Inc. --><path d="M0 96C0 78.3 14.3 64 32 64H416c17.7 0 32 14.3 32 32s-14.3 32-32 32H32C14.3 128 0 113.7 0 96zM0 256c0-17.7 14.3-32 32-32H416c17.7 0 32 14.3 32 32s-14.3 32-32 32H32c-17.7 0-32-14.3-32-32zM448 416c0 17.7-14.3 32-32 32H32c-17.7 0-32-14.3-32-32s14.3-32 32-32H416c17.7 0 32 14.3 32 32z"/></svg>
            <h3>Categorias</h3>
        </div>
        
        <div class="item-category">
            <img class="item-css-icon" src="../assets/categories-icons/smartphone-icon.svg" alt="">
            <p>Telefonia e Celulares</p>
        </div>
        <div class="item-category">
            <img class="item-css-icon" src="../assets/categories-icons/laptop-icon.svg" alt="">
            <p>Laptops e Computadores</p>
        </div>
        <div class="item-category">
            <img class="item-css-icon" src="../assets/categories-icons/wheel-icon.svg" alt="">
            <p>Automóveis</p>
        </div>
        <div class="item-category">
            <img class="item-css-icon" src="../assets/categories-icons/game-icon.svg" alt="">

            <p>Eletrônicos</p>
        </div>
        <div class="item-category">
            <img class="item-css-icon" src="../assets/categories-icons/toys-icon.svg" alt="">
            <p>Brinquedos e acessórios infantis</p>
        </div>
        <div class="item-category">
            <img class="item-css-icon" src="../assets/categories-icons/tools-icon.svg" alt="">
            <p>Ferramentas e Untecílios</p>
        </div>
        <div class="item-category">
            <img class="item-css-icon" src="../assets/categories-icons/watch-icon.svg" alt="">
            <p>Relógios e Joias</p>
        </div>
        <div class="item-category">
            <img class="item-css-icon" src="../assets/categories-icons/skipping-icon.svg" alt="">
            <p>Esportes e Fitness</p>
        </div>
        <div class="item-category">
            <img class="item-css-icon" src="../assets/categories-icons/manage-icon.svg" alt="">
            <p>Indústria e Comércios</p>
        </div>
        <div class="item-category">
            <img class="item-css-icon" src="../assets/categories-icons/fan-icon.svg" alt="">
            <p>Eletrodomésticos</p>
        </div>
        <div class="item-category">
            <img class="item-css-icon" src="../assets/categories-icons/brick-icon.svg" alt="">

            <p>Construção Civil</p>
        </div>
        <div class="item-category">
            <img class="item-css-icon" src="../assets/categories-icons/house-icon.svg" alt="">
            <p>Casa e Lazer</p>
        </div>
        <div class="item-category">
            <img class="item-css-icon" src="../assets/categories-icons/shoes-icon.svg" alt="">
            <p>Calçados</p>
        </div>
        <div class="item-category">
            <img class="item-css-icon" src="../assets/categories-icons/fragrance-icon.svg" alt="">
            <p>Perfumes</p>
        </div>


    </aside>

</template>
<script>
export default {
    data() {
        return {
            color :"blue"
        }
    },
}
</script>
<style>
h3{
    margin: 0;
}
aside{
    background-color: rgba(0, 0, 0, 0.1);
}
.categories-title-content{
    display: flex;
    flex-flow: row ;
    align-items: center;
    justify-content: flex-start;
    gap: 0.5em;
    padding: 1em;

}
.categories-container{

}

.categories-css{
    fill: rgb(33, 101, 204)
}
.item-category{
    padding: 0.5em 1em;
    display: flex;
    justify-content: flex-start;
    align-items: center;
}
.item-css-icon{
    width: 14px;
}
</style>
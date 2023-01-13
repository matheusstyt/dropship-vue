<template>
    <div class="profile-container">
        <div class="card-icon-content">
            <img src="../assets/tools/cart-icon.svg" alt="card">
        </div>
        <h4 class="profile-text">Criar conta</h4>
        <h4 class="profile-text">Entrar</h4>
        <h4 class="profile-text">Curtidas</h4>

    </div>
    
</template>
<style lang="scss">
.profile-container{
    padding: 0 3em;
    height: 100%;
    width: 40%;
    display: flex;
    align-items: center;
    gap: 1em;

}
.card-icon-content{
    height: 70%;
    aspect-ratio: 1/1;
    img{
        width: 80%;
        aspect-ratio: 1/1;
    }
}
.profile-text:hover{
    color: rgb(15, 69, 168);
    cursor: pointer;

}
</style>
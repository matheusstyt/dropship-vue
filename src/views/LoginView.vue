<template>
    <main class="main-login">
        <div class="back-content" @click="getReturn()"><img src="@/assets/tools/back-icon.svg" alt=""></div>
        <div class="registro-content" @click="getSign()"><p>Não tem cadastro?</p></div>

        <div class="login-container">
            <div class="login-slide">
            <img src="@/assets/tools/atro-cat.png" alt="">
            </div>
            <div class="login-content">
                <h2>Cadastrar</h2>
                <div class="input-p">
                    <label for="login">Usuário</label>
                    <input spellcheck="false" type="text" autocomplete="off" placeholder="Usuário" name="login" id="login">
                </div>
                <div class="input-p">
                    <label for="password">Senha</label>
                    <input spellcheck="false" type="password" autocomplete="off" placeholder="Senha" name="password" id="password">
                </div>
                <button id="btn-p">Cadastrar</button>
            </div>
        </div>
    </main>
</template>
<script>
export default {
    data(){
        return{
            
        }
    },
    methods:{
        getReturn(){
            window.history.back()
        }
    }
}
</script>
<style lang="scss">
// green => rgb(56, 216, 122);
$color_primary : rgb(229, 229, 236);
$color_secundary : rgb(25, 18, 41);
input:-webkit-autofill,
input:-webkit-autofill:hover, 
input:-webkit-autofill:focus, 
input:-webkit-autofill:active{
    background-color: rgba(255, 255, 255, 0.267);
    color: aliceblue;
}
input:-webkit-autofill{
    background-color: rgba(255, 255, 255, 0.267);
    -webkit-text-fill-color: rgb(82, 82, 82) !important;
    
}

.main-login{
    max-width: 100vw;
    width: 100vw;
    height: 100vh;
    position: relative;
    display: flex;
    align-items: center;
    justify-content: center;
    background-color: $color_primary;
    .back-content{
        position: absolute;
        width: 4em;
        aspect-ratio: 6/3;
        background-color: $color_secundary;
        border-radius: 2em;
        padding: 0.5em;
        top: 3.5%;
        left: 1%;
        img{
            width: 100%;
            height: 100%;
        }
    }
    .back-content:hover{
        background-color: rgb(56, 48, 85);
        box-shadow: 0px 0px 0.5em rgb(41, 41, 41);
    }
    .back-content:active{
        background-color: rgb(85, 73, 128);
        
    }
    .registro-content{
        background-color: $color_secundary;
        position: absolute;
        top: 3.5%;
        right: 1%;
        border-radius: 2em;
        padding: 0.7em;
        p{
            color: #fff;
            font-family: 'Consolas';
        }
    }
    .registro-content:hover{
        background-color: rgb(56, 48, 85);
        box-shadow: 0px 0px 0.5em rgb(41, 41, 41);
    }
    .registro-content:active{
        background-color: rgb(85, 73, 128);
        
    }
    .login-container{
        display: flex;
        align-items: center;
        justify-content: space-evenly;
        background-color: $color_secundary;
        box-shadow: 0px 0px 1em rgb(32, 32, 32);
        width: 60%;
        height: 70%;
        padding: 5em;
        border-radius: 2em;
        overflow: hidden;
        .login-slide{
            width: 40%;
            height: 100%;
            //background-color: rgba(10, 3, 51, 0.2);
            border-radius: 2em;
            img{
                width: 100%;
            }
        }
        .login-content{
            width: 40%;
            padding: 2em;
            border-radius: 1.4em;
            background-color: rgba(255, 255, 255, 0.15);
            box-shadow: 0px 0px 3em rgba(10, 3, 51, 1);
            h2{
                color: $color_primary;
                font-family: 'Consolas';
                font-size: 2em;
                text-shadow: 0px 0px 2em rgba(10, 3, 51, 1);
            }
            .input-p{
                margin: 0.4em;
                label{
                    font-family: 'Consolas';
                    color: antiquewhite;
                    display: block;
                    text-align: left;
                }
                input{
                    
                    box-shadow: 0px 0px 2em rgba(10, 3, 51, 1);
                    background-color: rgba(255, 255, 255, 0.267);
                    border: none;
                    color: rgb(230, 230, 230);
                    width: 95%;
                    margin: 0.4em 0;
                    border-radius: 1em;
                    height: 2.5em;
                    padding: 0.5em 1em;
                    font-family: 'Consolas';
                }
                input:hover{
                    box-shadow: 0px 0px 2em rgb(98, 89, 148);
                }
                :focus{
                    border: none;
                    box-shadow: 0px 0px 2em rgb(98, 89, 148);
                }
                input::selection{
                    background-color: rgb(171, 176, 230);
                }
                ::placeholder{
                    color: rgb(206, 206, 206);
                }    
            }
            #btn-p{
                width: 100%;
                height: 4em;
                margin: 1.6em 0;
                font-family: 'Consolas';
                font-weight: 800;
                border-radius: 1em;
                border: none;
                color: rgb(61, 61, 61);
                background-color: $color_primary;
                box-shadow: 0px 0px 2em rgba(10, 3, 51, 1);
            }
            #btn-p:hover{
                box-shadow: 0px 0px 2em rgb(98, 89, 148);
            }
            #btn-p:active{
                background-color: rgb(94, 231, 151);
            }
            
        }
    }

}

</style>
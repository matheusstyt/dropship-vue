<template>
    <main class="main-login">
        <div class="back-content"><img src="@/assets/tools/back-icon.svg" alt=""></div>
        <div class="login-container">
            <div class="login-slide">

            </div>
            <div class="login-content">
                <h2>LOGIN</h2>
                <div class="input-p">
                    <label for="login">Usuário</label>
                    <input type="text" autocomplete="off" placeholder="Usuário" name="login" id="login">
                </div>
                <div class="input-p">
                    <label for="password">Senha</label>
                    <input type="password" autocomplete="off" placeholder="Senha" name="password" id="password">
                </div>
                <button id="btn-p">LOGIN</button>
            </div>
        </div>
    </main>
</template>
<style lang="scss">
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
    background-color: rgb(56, 216, 122);
    .back-content{
        position: absolute;
        width: 4em;
        aspect-ratio: 6/3;
        background-color: rgb(33, 24, 49);
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
        box-shadow: 0px 0px 1em rgb(3, 51, 13);
    }
    .back-content:active{
        background-color: rgb(85, 73, 128);
    }
    .login-container{
        display: flex;
        align-items: center;
        justify-content: space-evenly;
        background-color: rgb(33, 24, 49);
        box-shadow: 0px 0px 3em rgb(3, 51, 13);
        width: 70%;
        height: 70%;
        padding: 5em;
        border-radius: 2em;
        overflow: hidden;
        .login-slide{
            width: 40%;
            height: 100%;
            background-color: rgba(10, 3, 51, 0.2);
            border-radius: 2em;
        }
        .login-content{
            width: 40%;
            padding: 2em;
            border-radius: 1.4em;
            background-color: rgba(255, 255, 255, 0.15);
            box-shadow: 0px 0px 3em rgba(10, 3, 51, 1);
            h2{
                color: rgb(56, 216, 122);
                font-family: 'Consolas';
                font-size: 2em;
            }
            .input-p{
                margin: 0.4em;
                label{
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
                    font-family: 'Arial';
                }
                input:hover{
                    box-shadow: 0px 0px 2em rgb(98, 89, 148);
                }
                input:focus{
                    border: none;
                    box-shadow: 0px 0px 2em rgb(98, 89, 148);
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
                background-color: rgb(56, 216, 122);
                box-shadow: 0px 0px 2em rgba(10, 3, 51, 1);
            }
            #btn-p:hover{
                box-shadow: 0px 0px 2em rgb(98, 89, 148);
            }
        }
    }

}

</style>
<template>
    <div class="container">
      <div class="contenedor-principal">
        <ul>
          <li v-for="(item,i) in redessociales" :key="i">
            <a :href="item.link" :class ="item.icono" target="_blank"></a>
          </li>
        </ul>
      </div>
    </div>
</template>

<script>
export default {
    name : 'RedesSociales',
    data(){
        return{
            redessociales : [
                { link : "https://www.facebook.com/trabajador.justarg", icono : "bton-facebook"},
                { link : "https://www.instagram.com/trabajadoresjust2021?igshid=1grcp39ip9bri", icono : "bton-instagram"}
            ]
        }
    }
}
</script>

<style scoped>

    .container {
        margin: -3px auto;
        background: #232931;
        width: 100%;
        position: relative;
        font-size: 2.5rem;
        display: flex;
        flex-direction: row;
        justify-content: center;
        border: 0;
    }

    .contenedor-principal{
        width: 60%;
        margin: 10px;
        border-radius: 6px;
        border: 1px solid #30363d;
    }

    ul{
        padding-inline-start: 0px;
    }

    li{
        height: 200px;
        width: 100%;
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
    }

    a:link, a:visited, a:active {
        text-decoration:none;
    }

    .pintar{
        border: 1px solid black;
    }

    .bton-facebook{
        margin: 5px;
        width: 10rem;
        height: 10rem;
        border: 0.3rem solid #efa94a;
        background-color: #efa94a;
        border-radius: 1rem;
        position: relative;
        top:0.1rem;
        left: 0.2rem;

    }


    .bton-facebook::before{
        content: "f";
        font-family: Facebook Letter Faces, Arial;
        color: #232931;
        font-size: 10rem;
        font-weight: bold;
        position: absolute;
        left: 3.2rem;
        top: 1.1rem;
    }


    .bton-instagram{
        width: 9rem;
        height: 9rem;
        border: 1rem solid #efa94a;
        background-color: transparent;
        border-radius: 2rem;
        position: relative;
        top:0.1rem;
        left: 0.2rem;
        margin: 0 10px;
    }


    .bton-instagram::before{
        content: "";
        width: 5rem;
        height: 5rem;
        border: 0.5rem solid #efa94a;
        background-color: transparent;
        border-radius: 50%;
        position: absolute;
        left: 1.5rem;
        top: 1.6rem;
    }

    .bton-instagram::after{
        content: "";
        width: 2rem;
        height: 2rem;
        background: #efa94a;
        border-radius: 1rem solid #efa94a;
        border-radius: 80%;
        position: absolute;
        right: 0.4rem;
        top: 0.5rem;
    }

    .corazon{
        background-color: red;
        display: inline-block;
        height: 1rem;
        width: 1rem;
        margin: 0 10px;
        position: relative;
        top: 0.3rem;
        transform: rotate(-45deg);
    }

    .corazon::before, .corazon::after{
        content: "";
        background-color: red;
        border-radius: 50%;
        width: 1rem;
        height: 1rem;
        position: absolute;
    }

    .corazon::before{
        top: -0.5rem;
        background-color: red;
    }

    .corazon::after{
        top: 0 ;
        left: 0.5rem;
        background-color: red;
    }




</style>

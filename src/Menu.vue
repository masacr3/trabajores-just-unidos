<template>
  <div class="conteiner">
    <div class="bton-menu" @click='desplegar = !desplegar'></div>
    <ul v-show="desplegar">
      <li v-for="i in 10" :key="i">menu {{i}}</li>
    </ul>
  </div>
</template>

<script>

export default {
  name: 'Menu',
  data(){
    return{
      desplegar : false
    }
  },
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

  .bton-menu{
    width: 5rem;
    height: 5rem;
    background-color: #efa94a;
    border: 0.3rem solid #efa94a;
    border-radius: 1rem;
    position: absolute;
    top: 40vh;
    left: -10px;
  }

  .bton-menu::after{
    content: "";
    width: 5.5rem;
    height: 5.6rem;
    background-color: #efa94a;
    border-radius: 50%;
    position: absolute;
    left: 1.9rem;
    top: -0.3rem;
  }

  .bton-menu::before{
    z-index: 1;
    content: "Menu";
    font-family: Facebook Letter Faces, Arial;
    color: #232931;
    font-size: 2rem;
    font-weight: bold;
    position: absolute;
    left: 1rem;
    top: 1.4rem;
  }
</style>

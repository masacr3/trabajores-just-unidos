<template>
  <div id="app">
    <Menu></Menu>
  </div>

</template>

<script>
import TimeLine from './TimeLine.vue'
import RedesSociales from './RedesSociales.vue'
import Menu from './Menu.vue'

export default {
  name: 'app',
  data () {
  },
  components:{
    'TimeLine' : TimeLine,
    'RedesSociales' : RedesSociales,
    'Menu' : Menu
  }

}
</script>



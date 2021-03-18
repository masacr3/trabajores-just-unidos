<template>
  <div id="app">
    <TimeLine></TimeLine>
    <RedesSociales></RedesSociales>
  </div>

</template>

<script>
import TimeLine from './TimeLine.vue'
import RedesSociales from './RedesSociales.vue'

export default {
  name: 'app',
  data () {
  },
  components:{
    'TimeLine' : TimeLine,
    'RedesSociales' : RedesSociales
  }

}
</script>


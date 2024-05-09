<template>
  <div>
   <carousel-comp></carousel-comp>
  </div>
</template>

<script>
import CarouselComp from './CarouselComp.vue'
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  },
  components:{
    CarouselComp,
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>

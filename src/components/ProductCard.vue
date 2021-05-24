<template>
  <div>
    <img :src="card.thumb" :alt="card.type">
    <h4>
       {{card.type}}
    </h4>
   

  </div>
</template>

<script>
export default {
  name: 'ProductCard',
  props:{
    card: Object
  }

}
</script>

<style lang="scss" scoped>
h4{
  color: white;
}

</style>
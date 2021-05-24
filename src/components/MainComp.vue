<template>
  <main>

   
   <div class="container">
        <ProductCard
          v-for="(product, index) in products"
     :key="index"
     :card="product"
     
     />
     <h3>
      
     </h3>
      

   </div>
  
  
     
     
    
     
     
    
   
     

    
 

  </main>
</template>

<script>
import  products from "@/assets/data/dc-comics.js";
import ProductCard from "@/components/ProductCard";
export default {
  components: { ProductCard },
  name: 'MainComp',

  data(){
    return{
      products
    }
  }

}
</script>

<style lang="scss" scoped>
main{
  width: 100%;
  height: 100%;
  background-color:black;
}
.container{
  display: flex;
  flex-wrap: wrap;
  justify-content:space-around ;
  
}
h3{
  color: white;
}

</style>
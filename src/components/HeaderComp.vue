<template>
<header>
  <div class="cols">
    <div class="sx"></div>
    <div class="dx">
      <ul>
     <li v-for="(link, index) in links"
     :key="index"
    
      >
      <a :class="{'active': link.current}" :href="link.url">{{link.text}}</a>
      
      
     

     </li>
   </ul>

    </div>
   
   
   
  </div>

</header>
  
</template>

<script>
import links from "@/assets/data/link-header.js";
export default {
  name: 'HeaderComp',
  components:{
    

  },
  

  data(){
    return{
      links
    }
  },
  mounted(){
    console.log(links);
  }

}

</script>

<style lang="scss" scoped>
.cols{
  width: 100%;
  
}
ul{
  list-style: none;
  
  li{
    cursor: pointer;
    display: inline-block;
     padding-left: 10px;
     ;
     a{
       text-decoration: none;
       color: rgb(239, 243, 243);
       &:hover,
       &:active{
         background-color: rgb(204, 203, 197);
         opacity: .5;
       }
     }
  }
 
}
header{
  padding: 5px;
  width: 100%;
  height: 80px;
  line-height: 80px;
  background-color: rgb(32, 32, 30);
 
}

.sx{
  float: left;
}
.dx{
  float: right;
}

</style>
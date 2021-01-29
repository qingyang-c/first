<template>
  <div id="app">  
    <ComHeader></ComHeader>
    <router-view class="main" />
    <ComFooter></ComFooter>
 </div>
    
</template>
<script>
import ComHeader from "./components/ComHeader";
import ComFooter from "@/components/ComFooter";
export default {
  components: {
    ComHeader,
    ComFooter,
  },
};
</script>
<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
   .main{
     margin: 1rem 0;
   }
}


  a {
    font-weight: bold;
    color: #2c3e50;

    
  }

</style>

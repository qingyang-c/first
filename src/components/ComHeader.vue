<template>
   <header :style="{backgroundColor:curMenu.bgColor}">
      <span @click="goHome">《 首页</span>
      {{curMenu.name}}
    </header>
        
</template>

<script>
    import { mapState, mapMutations } from "vuex";
    export default {
      computed: {
      ...mapState(["curMenu"]),
    },  
    methods:{
        ...mapMutations(["setMenu"]),
        goHome() {
            this.$router.push("/");
            this.setMenu({
            name: "剧集",
            bgColor: "rgb(243, 113, 113)",
            });
        },
    }
 };

   
</script>

<style lang="scss" scoped>
header { 
 background:rgb(243, 113, 113);
  position: fixed;
  top:0;
  width: 100%;
  height: 1rem;
  line-height: 1rem;
  text-align: center;
 
  span {
    position: absolute;
    left: 0;
  }
}
</style>
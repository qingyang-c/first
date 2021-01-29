<template>
   <footer :style="{backgroundColor:curMenu.bgColor}">
       <div v-for=" menu in menuList" :key="menu.path" @click="switchMenu(menu)">
         <router-link :to="menu.path">{{menu.name}}</router-link>
       </div> 
   </footer>
      
    
</template>

<script>
import { mapState, mapMutations } from "vuex";
    export default {
        computed: {
        ...mapState(["curMenu"]),
  },
         data(){
            return{
                menuList:[
                    { path: "/", name: "剧集", bgColor: "rgb(243, 113, 113)" },
                    { path: "/music", name: "音乐", bgColor: " rgb(118, 247, 167)" },
                    { path: "/book", name: "书籍", bgColor: "rgb(109, 214, 247)" },
                    
                ]
            }
        },

        methods:{
            ...mapMutations(["setMenu"]),
            switchMenu(menu) {
            this.setMenu(menu)
           },  
        }
        
    }
</script>

<style lang="scss" scoped>
footer {
  display: flex;
  background: rgb(243, 113, 113);
  justify-content: space-around;
  position: fixed;
  bottom: 0rem;
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
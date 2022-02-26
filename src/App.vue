<template>
    <navi @="handlerclear"  :tabs="tabs"></navi>
    <navi :tabs="tab2"/>       
</template>





<script >
import navTabsVue from "./components/nav-tabs.vue"
    export default {

      data() {
        return {
            tabo:true ,
          tabs: [
                  {
                      title: 'home',
                      content: 'home content'
                  },

                  {
                      title: ' about',
                      content: 'about content'
                  } ,
                  {
                    title: ' contact',
                      content: 'contact content'
                  }
              ] ,
                tab2 :[
                    {
                      title: 'Garbage room',
                      content: 'Garbage Garbage Garbage'
                  },

                  {
                      title: ' women Part',
                      content: 'women women women'
                  } ,
              ]
              } 
            } , 

            components :{
              'navi': navTabsVue
            } , 

            methods:{
              handlerclear(buttonState){
                this.tabs =[]  
                buttonState ='cansel'
                 
              }
            }
    }
</script>


<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

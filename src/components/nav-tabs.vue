<template>
      <div class="container ">
        <h2>tab menu</h2>   
 
        <ul class="nav nav-tabs" id="myTab" role="tablist">
            <li class="nav-item" role="presentation" v-for="{title} in tabs">
                <button class="nav-link" :class="{'active' : curenttab == title}" id="home-tab" type="button" @click="curenttab = title"> {{title}} </button>
            </li>
            <button @click="$emit('clear' ,buttonState)">{{buttonState}}</button>
        </ul>

        <div class="tab-content p-3 " id="myTabContent ">
            <div class="tab-pane fade show active " v-for=" {title , content} in tabs" v-show="curenttab == title">{{content}}</div>
        </div>

    </div>
</template>



<script>
    export default {
            data() {
            return {
                buttonState:'clear' ,
                curenttab: 'home'
            }
        } , 


           props:{
               tabs:{
                   type :Array , 
                   required :true
               }
           } ,
           //اعتبار سنجی امت ها !!!! ===>>
            emits:{
                'clear' :function (params) {
                    if (params =='clear') {
                        return console.log('its clear');
                    }
                }
            }

  /*          methods:{
               clearData(){
                   this.$emit('clear')
               }
           } */
               //We dont need to handle emit method from `methods:{}` part necesarlly !!;its handdleable even in inline html tag
    }
</script>
        
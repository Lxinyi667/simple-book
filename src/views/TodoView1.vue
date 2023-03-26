<template>
    <div class="layout">
        <div v-for="item in items" :key="item.id">
            <TodoItem :item="item"/>
            <span>111</span>
        </div>
    </div>
</template>

<script setup>
   import TodoItem from '@/components/TodoItem.vue'
   import ItemService from '@/services/ItemService.js'

   import { ref , onMounted } from 'vue'
//    import axios from 'axios'
    const items = ref({})
    // let list = reactive([])
    // let items = reactive([
    
    //    {
    //         "id":1,
    //         "title":"Vue3学习",
    //         "date" :"2023-03-24",
    //         "logo":"../assets/images/RealWorldVue3.png",
    //         "location":"南京",
    //         "finished":true
    //     },
    //      {
    //         "id":2,
    //         "title":"Pinia学习",
    //         "date" :"2023-03-24",
    //         "logo":"../assets/images/RealWorldVue3.png",
    //         "location":"苏州",
    //         "finished":true
    //     },
    //     {
    //         "id":3,
    //         "title":"TS学习",
    //         "date" :"2023-03-24",
    //         "logo":"../assets/images/RealWorldVue3.png",
    //         "location":"合肥",
    //         "finished":true
    //     }
    // ])
 
    onMounted( ()=>{
       ItemService.getTodoItems()
        .then((res) =>{
            console.log(res.data)
            items.value = res.data
        })
        .catch((error)=>{
            console.log(error)
        })
    })
</script>

<style  scoped>
.layout {
  display: flex;
  flex-wrap: wrap;
  width: 90%;
  margin: 0 auto;
}
.layout div {
  flex: 1;
}
</style>
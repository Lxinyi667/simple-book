<template>
    <div class="row">
        <div class="aside">
            
                <ul>
                    <li>
                        <a href="/backend">
                            <span data-type="backend">后端</span>
                        </a>
                    </li>
                    <li>
                        <a href="/frontend">
                            <span data-type="backend">前端</span>
                        </a>
                    </li>
                    <li >
                        <a href="/techareas/backend">
                            <span data-type="backend">Andriod</span>
                        </a>
                    </li>
                    <li>
                        <a href="/ios">
                            <span data-type="backend">IOS</span>
                        </a>
                    </li>
                
                    <li>
                        <a href="/techareas/backend">
                            <span data-type="backend">人工智能</span>
                        </a>
                    </li>
                    <li>
                        <a href="/techareas/backend">
                            <span data-type="backend">数据库</span>
                        </a>
                    </li>
                    <li>
                        <a href="/techareas/backend">
                            <span data-type="backend"></span>
                        </a>
                    </li>
                </ul>
            
            
        </div>
        
        <!-- s -->
         <!-- 以及二级菜单所对应的页面 -->
         <main class="cont">
            <router-view></router-view>
        </main>

    </div>
</template>

<script setup>
//    import TodoItem from '@/components/TodoItem.vue'
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
    });
    
</script>

<style  scoped>
*{
    margin:0;
    padding:0;
    list-style: none;
    text-decoration: none;
    color: black;
    margin: 0 auto;
}
.aside{
    margin:30px 40px;
    width: 130px;
    height: 300px;
    padding-left: 30px;
    box-shadow: 1px 5px 5px #ccc;
    float: left;
}
.aside a{
    padding: 16px 15px;
    font-size: 15px;
    display:block;
}
a{
    cursor: pointer;
}
span:hover{
    color: blue;
}
.cont{
    float: left;
    width: 600px;
    height: 300px;
    margin:30px 40px;
    box-shadow: 1px 5px 5px #ccc;
}
</style>
<template>
    
    <RouterLink class="item-link" :to="{name:'item-details',params:{id:item.id}}">
            <div class="card" :class="{finished:item.finished}">
                <h3>{{ item.title }}</h3>
                <p class="p1">{{ item.date }}</p>
                <p class="p2">{{ item.msg }}</p>
                <!-- <img :src="item.logo" :alt="item.title"> -->
                <!-- <div class="status">
                    <p v-if="item.finished" class="finished">结束</p>
                    <p v-else class="unfinished">进行中</p>
                </div> -->
                <img :src="item.logo" :alt="item.title">
            </div>
           
    </RouterLink>
   
</template>

<script setup>
// import { ref } from 'vue';
 defineProps({
    item:{
        type:Object,
        required: true,
    },
})

</script>

<style  scoped>
*{
    margin: 0;
    padding: 0;
    list-style: none;
    text-decoration: none;
    color: black;
}
    .card{
        height: 150px;
        width: 60%;
        border-bottom: 1px solid gray;
        margin: 20px;
        /* padding-top: 10px; */
        transition-duration: 300ms;
        padding:20px  0 0 30px;
        
    }
    .card .p1{
        font-size: 12px;
        color: gray;
    }
    .card .p2{
        font-size: 14px;
    }
    /* .card:hover{
        margin-top: -10px;
        transition-duration: 300ms;
    } */
    .card img{
        margin-top: 30px;
        height: 30px;
        /* width: 100px; */
    }
    .status{
        margin-top: 20px;
    }
    .finished{
        -webkit-filter: grayscale(1); /* Chrome, Safari, Opera */
        filter: grayscale(1);
    }
    .unfinished{
        color: rgb(19, 75, 124);
    }
    .item-link {
    color: #2c3e50;
    text-decoration: none;
    }
</style>
<template>
    <div v-if="item" class="layout">
        <div>
            <img :src="item.logo" :alt="item.title">
        </div>
        <div>
            <h2>{{ item.title }}</h2>
            <p>{{ item.description }}</p>
            <p>
                <span class="meta">{{ item.location }}</span>
                <span class="meta">{{ item.date }}</span>
            </p>
        </div>
    </div>
</template>

<script setup>
    import { ref , onMounted } from 'vue'
    import ItemService from '@/services/ItemService.js'

   const props = defineProps({
    id:{
        type : String,
        required : true,
    },
   })
   let item = ref({})

//    const idd = ref(1)
   onMounted(() =>{
    ItemService.getItem(props.id)
    .then((res) =>{
        console.log(res.data)
        item.value = res.data
    })
    .catch((error)=>{
        console.log(error)
    })
   })
</script>

<style scoped>
    *{
        margin: 0;
        padding: 0;
        list-style: none;
    }
    .layout{
     display: flex;
     box-shadow: 1px 2px 2px #ccc;
     padding-top: 50px;
    }

    .layout div {
    flex: 1;
    padding: 20px;
    }

    .layout div p {
    padding-top: 50px;
    line-height: 2;
    }
    .layout .meta {
    font-size: 14px;
    color: #ccc;
    margin-right: 10px;
    }

</style>
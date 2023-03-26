<template>
    <div>
        <!-- {{item.id}} -->
        <!-- {{testData.id}} -->
        <h1 style="position: relative;left: 300px;">详细界面</h1>
        <div class="card">

            <div>
                <img :src="item.avatar" style="width: 200px;height: 200px;">
            </div>
            <div style="padding-left: 30px;">
                <h2>{{ item.title }}</h2>
                <p>{{ item.date }}</p>
                <p>{{ item.description }}</p>
            </div>

        </div>
    </div>
</template>

<script setup>
import ItemService from '@/services/ItemService.js'
import { onBeforeMount, onMounted, ref } from 'vue'

const props = defineProps({
    id: {
        type: String,
        require: true,
    }
})

let item = ref(null);


// onMounted(() => {
//     ItemService.getItem(props.id)
//         .then((resp) => {
//             console.log(resp.data);
//             item.value = resp.data;
//             // jsonObj = resp.data;
//         })
//         .catch((error)=>{
//             console.log(error);
//         })
// })

onBeforeMount(() => {
    ItemService.getItem(props.id)
        .then((resp) => {
            console.log(resp.data);
            item.value = resp.data;
            // jsonObj = resp.data;
        })
        .catch((error) => {
            console.log(error);
        })
})

// let item = ref(jsonObj);

// console.log(item);


</script>

<style  scoped>
.card {
    display: flex;
    width: 700px;
    height: 250px;
    text-align: center;
    padding-top: 20px;
    padding-left: 10px;
    padding-right: 10px;
    border: 1px solid lightgray;
    box-shadow: 10px 5px 5px rgba(0, 0, 0, 0.2);
    margin-bottom: 20px;
    border-radius: 5px;
    background-color: rgba(187, 185, 48, 0.6);
}
</style>
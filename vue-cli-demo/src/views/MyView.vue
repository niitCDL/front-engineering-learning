<template>
    <div>
        asasas
        asasas
        <TodoItem :item="items"></TodoItem>
    </div>
</template>

<script setup>
import TodoItem from '@/components/TodoItem.vue'
import ItemService from '@/services/ItemService.js'
import { reactive, onMounted, ref } from 'vue'
import axios from 'axios'
// const item = reactive([{
//     id: 1,
//     title: 'Vue3学习',
//     data: '2023-03-24',
//     description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Hic, dolore vitae. Nesciunt animi ratione at obcaecati inventore laboriosam exercitationem quas expedita fugit, consequatur mollitia, eius possimus praesentium corrupti. Nihil, velit.',
//     avatar:'/src/assets/images/1.png'
// }, {
//     id: 2,
//     title: 'Java学习',
//     data: '2023-03-24',
//     description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Hic, dolore vitae. Nesciunt animi ratione at obcaecati inventore laboriosam exercitationem quas expedita fugit, consequatur mollitia, eius possimus praesentium corrupti. Nihil, velit.',
//     avatar:'/src/assets/images/2.png'

// }, {
//     id: 3,
//     title: 'Python学习',
//     data: '2023-03-24',
//     description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Hic, dolore vitae. Nesciunt animi ratione at obcaecati inventore laboriosam exercitationem quas expedita fugit, consequatur mollitia, eius possimus praesentium corrupti. Nihil, velit.',
//     avatar:'/src/assets/images/3.png'
// },{
//     id: 4,
//     title: 'PHP学习',
//     data: '2023-03-24',
//     description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit. Hic, dolore vitae. Nesciunt animi ratione at obcaecati inventore laboriosam exercitationem quas expedita fugit, consequatur mollitia, eius possimus praesentium corrupti. Nihil, velit.',
//     avatar:'/src/assets/images/4.png'
// },])

let items = ref(null);

onMounted(() => {
    ItemService.getTodoItems()
        .then((resp) => {
            items.value = resp.data;
        })
        .catch((error) => {
            console.log(error);
        })
})


// onMounted(() => {
//     axios.get('http://localhost:3000/items').
//         then((resp) => {
//             console.log(resp.data);
//             item.value = resp.data;
//             console.log(item)
//         })
//         .catch((error)=>{
//             console.log(error)
//         })
// })


</script>

<style lang="scss" scoped></style>
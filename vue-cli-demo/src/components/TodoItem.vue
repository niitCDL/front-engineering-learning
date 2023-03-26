<template>
  <template v-for="(ele,index) in item">
    <RouterLink :to="{name:'item-details',params:{id:ele.id}}" class="hrefClass2">
    <div class="card">

        <div>
          <img :src="ele.avatar" style="width: 200px;height: 200px;">
        </div>
        <div style="padding-left: 30px;">
          <h2>{{ ele.title }}</h2>
          <p>{{ ele.date }}</p>
          <p>{{ ele.description }}</p>
        </div>

    </div>
  </RouterLink>

  </template>
</template>

<script setup>

defineProps({
  item: {
    type: Object,
    required: true
  }
})


</script>

<style scoped>
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
.hrefClass2{
  display: block;
  text-decoration: none;
  outline: none;
}
.hrefClass2:active{
  color: #00BFFF;
}
</style>
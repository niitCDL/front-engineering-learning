<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
<!-- 
    <div>

      <nav>
        <RouterLink to="/" class="hrefClass">Home</RouterLink>
        <RouterLink to="/my" class="hrefClass">itemList</RouterLink>
      </nav>
    </div> -->
    <main>
      <RouterView />
    </main>
</template>

<style scoped>
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
main{
  width: 85%;
  min-height: 80vh;
  margin: 150px auto;
  border: 1px solid lightgray;
  border-radius: 5px;
  padding-left: 450px;
  padding-top:30px;

}

nav {
  width: 100%;
  height: 100px;
  font-size: 50px;
  position: fixed;
  line-height: 100px;
  top: 0;
  left: 0;
  text-align: center;
  background-color: rgba(128,0,128);
}

.hrefClass{
  display: inline-block;
  text-decoration: none;
  margin-right: 30px;
  color: gray;
}
.router-link-active{
  color: #00BFFF;
}
</style>

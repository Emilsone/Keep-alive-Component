<template>
  <div id="app">
    <h1>ShoppingList</h1>
    <div>
      <button class="btn-item">Old Item</button>
      <button class="btn-item">New Item</button>
    </div>

    <OldItem />
  </div>
</template>

<script>
// In this article we will build a simple shopping cart item

// import HelloWorld from './components/HelloWorld.vue'
import OldItem from "./components/OldItem.vue";

export default {
  name: "App",
  components: {
    OldItem,
  },
};  
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Work+Sans&display=swap");
#app {
  font-family: "Work Sans", sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.btn-item {
  background-color: rgb(139, 221, 139);
  margin: 10px;
  padding: 10px 15px;
}
</style>


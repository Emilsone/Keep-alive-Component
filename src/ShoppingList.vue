<template>
  <div id="app">
    <h1 class="text-3xl bold py-3">ShoppingList</h1>
    <div>
      <button
        v-for="tab in tabContents"
        :key="tab"
        @click="component = tab"
        class="btn-item"
      >
        {{ tab }}
      </button>
    </div>
   
  </div>
</template>

<script>



import OldItem from "./components/OldItem.vue";
import NewItem from "./components/NewItem.vue";

export default {
  name: "App",
  components: {
    OldItem,
    NewItem,
  },
  data() {
    return {
      tabContents: ["OldItem", "NewItem"],
      component: "OldItem",
    };
  },
};
</script>

<style>
// What are Dynamic Component?


 




//Dynamic Component Output


// Vue Keep-alive

// How does Vue Keep-alive work?
// in vue terminlogy kee-alive is what we call the abstract  element which means it does not create a dom or show up in component heirarchy

// import HelloWorld from './components/HelloWorld.vue'
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
  background-color: #c50d1d;
  margin: 10px;
  padding: 10px 15px;
  color: white;
}
</style>


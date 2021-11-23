<template>
  <div class="Employee">
    <form action="">
      <input type="text" placeholder="New List" class="input-bg p-4 my-4">
    </form>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

.input-bg{
  background-color:#F9F5FF;
  outline:#F9F5FF ;
  border:2px solid rgb(197, 194, 194)
}
</style>

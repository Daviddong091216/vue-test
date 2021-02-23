<template>
  <div>
    <div v-bind:key="item1.id" v-for="item1 in todos2">
      <TodoItem1 v-bind:item2="item1" />
    </div>
  </div>
</template>
<script>
import TodoItem1 from './TodoItem';
export default {
  name: "Todos",
  components:{
      TodoItem1
  },
  props: ["todos2"],
};
</script>
<style scoped>
</style>
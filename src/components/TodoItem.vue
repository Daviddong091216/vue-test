<template>
  <div class="todo-item" v-bind:class="{'is-complete':item2.completed}">
    <p>
      <input type="checkbox" v-on:change="markComplete">  
        {{item2.title}}</p>
  </div>
</template>
<script>
export default {
  name: "TodoItem",
  props: ["item2"],
  methods:{
      markComplete(){
          console.log(this.item2.completed);
        //   this.item2.completed = !this.item2.completed;
          
      }
  }
};
</script>
<style scoped>
.todo-item {
  background: #f4f4f4;
  padding: 10px;
  border-bottom: 1px #ccc dotted;
}
.is-complete {
    text-decoration: line-through;
}
</style>
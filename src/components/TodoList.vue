<template>
  <div>
    <ul>
      <TodoItem 
        v-for="t in todos" 
        v-bind:todo="t" 
        v-bind:key="t.id"
        v-on:remove-todo="remTodo" /> <!-- Мы получили событие remove-todo и передаем его обработчику remTodo -->
    </ul>
  </div>
</template>


<script>
import TodoItem from "@/components/TodoItem";
export default {
  props: ["todos"],
  components: {
    TodoItem,
  },
  methods: {
    remTodo(id){
      this.$emit('r-todo', id)
    }
  }
};
</script>

<style scoped>
  ul {
    list-style: none;
    margin: 0;
    padding: 0;
  }
</style>
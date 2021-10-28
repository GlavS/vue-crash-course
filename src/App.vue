<template>
  <div id="app">
    <h1>Todo application(c)V.Minin</h1>
    <hr />
    <TodoList 
      v-bind:todos="todos"
      @remove-todo="removeTodo" />

    <!--<img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld msg="Welcome to Your Vue.js App"/>    was default -->
  </div>
</template>

<script>
//import HelloWorld from './components/HelloWorld.vue' //was default
import TodoList from "@/components/TodoList";

export default {
  name: "App",
  data() {
    return {
      todos: [
        { id: 1, title: "Купить хлеб", completed: false },
        { id: 2, title: "Купить масло", completed: false },
        { id: 3, title: "Купить пиво", completed: false },
      ],
    };
  },
  components: {
    //HelloWorld //was default
    TodoList,
  },
  methods: {
    removeTodo(id){
      this.todos = this.todos.filter(t => t.id !== id)
    }
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

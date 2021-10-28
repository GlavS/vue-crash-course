<template>
  <div>
    <ul>
      <TodoItem v-for="t in todos" v-bind:todo="t" v-bind:key="t.id" />
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
};
</script>
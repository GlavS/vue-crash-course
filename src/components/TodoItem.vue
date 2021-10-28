<template>
  <div>
    <span>
      <input type="checkbox" />
      <strong>{{ todo.id }}</strong>
      {{ todo.title }}
    </span>
    <button>&times;</button>
  </div>
</template>

<script>
export default {
  props: {
    todo: {
      type: Object,
      required: true,
    },
  },
};
</script>
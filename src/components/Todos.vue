<template>
  <ul>
    <Todo v-for="(todo, index) in todos" :key="index" :todo="todo" :index="index" @delete-todo="test"/>
  </ul>
</template>

<script>
import Todo from './Todo'

export default {
  name: 'Todos',
  props: {
    todos: Array,
  },
  components: {
    Todo
  },
  methods: {
    test(index) {
      this.$emit('delete-todo', index)
    }
  }
}
</script>

<template>
<h1>ToDo App</h1>
<ToggleButton :showForm="showForm" @toggle-form="toggle" />
<p>Todo Count: {{ this.todos.length }}</p>
</template>

<script>
import ToggleButton from './Toggle'
export default {
  emits: ["toggle"],
  name: 'Header',
  props: {
    showForm: Boolean,
    todos: Array,
  },
  components: {
    ToggleButton
  },
  methods: {
    toggle() {
      this.$emit('toggle', this.showForm)
    }
  }
}
</script>

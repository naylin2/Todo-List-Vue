<template>
  <Header :showForm="showForm" :todos="todos" @toggle="toggle"/>
  <Form :formInput="formInput" :showForm="showForm" @addTodo="addTodo"/>
  <Todos :todos="todos" @delete-todo="deleteTodo"/>
</template>

<script>
import Todos from './components/Todos'
import Header from './components/Header'
import Form from './components/Form'

export default {
  name: "App",
  components: {
    Todos,
    Header,
    Form,
  },
  data() {
    return {
      showForm: true,
      todos: []
    }
  },
  created() {
    this.todos = [
      'Todo 01', 'Todo 02'
    ]
  },
  methods: {
    addTodo(formInput) {
      if (formInput.length > 0) {
        this.todos.push(formInput)
      }
    },
    deleteTodo(index) {
      this.todos.splice(index, 1)
    },
    toggle() {
      this.showForm = !this.showForm
    }
  }
};
</script>

<style>
</style>

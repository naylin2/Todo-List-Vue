<template>
  <form v-if="showForm">
    <input type="text" v-model="formInput" />
    <input type="submit" v-on:click.prevent="$emit('addTodo',formInput); clear();" />
  </form>
  <p>Current: {{ formInput }}</p>
</template>

<script>
export default {
  emits: ['formInput'],
  name: 'Form',
  data() {
    return {
      formInput: '',
    }
  },
  props: {
    showForm: Boolean,
  },
  methods: {
    clear() {
      this.formInput = ''
    }
  }
}
</script>

<template>
  <li>
    <p>
      {{ index }}: {{ todo }}
      <span><button @click="$emit('delete-todo', index)">X</button></span>
    </p>
  </li>
</template>

<script>
export default {
  name: 'Todo',
  props: {
    todo: String,
    index: Number,
  }
}
</script>

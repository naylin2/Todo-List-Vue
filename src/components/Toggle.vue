<template>
  <button @click="$emit('toggle-form')">
    {{ showForm ? "Hide" : "Show" }} Form
  </button>
</template>

<script>
export default {
  name: 'ToggleButton',
  props: {
    showForm: Boolean,
  }
}
</script>

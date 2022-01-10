<template>
  <button @click="$emit('toggle-form', showForm)">
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

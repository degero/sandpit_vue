<template>
<div>
    <li>{{todo.label}}</li>
</div>
</template>

<script>
export default {
  name: 'Todo',
  props: ['todo']
}
</script>

<style scoped>

</style>
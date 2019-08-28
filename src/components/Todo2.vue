<template>
 <div v-if="items">
    <p>My Todo list has {{items.length}} items</p>
    <ul>
      <li v-for="item in items" v-bind:key="item.id">{{item.label}}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'Todo2',
  props: ['items']
}
</script>

<style scoped>

</style>
<template>
  <div id="app">
    <HelloWorld msg="World"/>
    <div v-if="TodoItems">
      <p>My Todo list using singular binding li component items</p>{{TodoItems.length}}
      <ul>
        <Todo v-for="item in TodoItems" v-bind:todo="item" v-bind:key="item.id"></Todo>
      </ul>
    </div>
    <Todo2 v-bind:items="TodoItems"></Todo2>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import Todo from './components/Todo.vue'
import Todo2 from './components/Todo2.vue'

export default {
  name: 'app',
  components: {
    HelloWorld,
    Todo,
    Todo2
  },
  data: function() { // this would be a async call to get data
    return { TodoItems:  [{id: 1, label: 'Clean bicycle'},{ id: 2, label: 'Do tax'}]};
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

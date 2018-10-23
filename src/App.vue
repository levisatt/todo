<template>
  <div id="app">
    <new-item @add-item="addItem" />
    <list :items="todos" @delete="deleteItem"></list>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import List from './components/list.vue'
import NewItem from "./components/newItem"

export default {
  name: 'app',
  components: {
    NewItem,
    List,
    HelloWorld,
  },

  data:()=> ({
    message:'echo echo',
    todos:[],
  }),

  methods: {
    deleteItem(index){
      this.todos.splice(index, 1)
      this.updateStorage()
    },

    addItem(item){
      this.todos.push({...item})
      this.updateStorage()
    },

    updateStorage(){
      localStorage.setItem('todos', JSON.stringify(this.todos))
    }
  },

  mounted(){
    this.todos = JSON.parse(localStorage.getItem('todos')) || []
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

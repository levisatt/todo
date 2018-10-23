<template>
  <div id="app">
    <!--<img alt="Vue logo" src="https://i.imgur.com/KpfRRdc.png">-->
    <list :items="todos"></list>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import List from './components/list.vue'

export default {
  name: 'app',
  components: {
    List,
    HelloWorld,
  },

  data:()=> ({
    message:'echo echo',
    todos:[
      { message: 'Foo'},
      { message: 'Bar'},
    ],
  })

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

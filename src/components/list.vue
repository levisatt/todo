<template>
  <div>
    <div v-for="(item,index) in items">
      {{item.message}}
      <button v-on:click="$emit('delete', index)">Delete</button>
    </div>

  </div>
</template>


<script>
  import Item from './item.vue'

  export default {


    props: {items: Array}
  }
</script>
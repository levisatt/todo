<template>
  <div>
    <div v-for="(item,index) in items">
      {{item.message}}
      <button @click="$emit('delete', index)">Delete</button>
    </div>

  </div>
</template>

<script>
  export default {
    props: {items: Array}
  }
</script>

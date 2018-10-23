<template>
    <div>
    <input type="checkbox"
    v-model="item.done"/>
    <span>
        {{item.message}}
    </span>

    <button @click="$emit('delete', item.id)"></button>
    </div>
</template>


<script>
    export default{
      props:{
        item:Object
      },

    }
</script>
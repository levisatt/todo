<template>
    <div class="new-item">
        <label for="message">Message</label>
        <input id="message" name="message" @keyup="checkEnter" v-model="item.message" />
        <button type="submit" @click="addNewItem">Add</button>
    </div>
</template>

<script>
  export default {
    data:() => ({
      item: {
        message: null,
      }
    }),

    methods: {
      checkEnter($event){
        console.log($event)
        if($event.keyCode === 13){
          // we hit the enter key
          this.addNewItem()
        }
      },

      addNewItem(){
        this.$emit('add-item', this.item)
        this.item.message = null
      }
    }
  }
</script>

<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <p>
      This is your To-Do list! Please list all of the things<br>
      you have to do below.
    </p>
    <!--<h3>Installed CLI Plugins</h3>
    <ul>
      <li><a href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-babel" target="_blank" rel="noopener">babel</a></li>
      <li><a href="https://github.com/vuejs/vue-cli/tree/dev/packages/%40vue/cli-plugin-eslint" target="_blank" rel="noopener">eslint</a></li>
    </ul>
    <h3>First App</h3>
    <ul>
      <li><a href="https://vuejs.org" target="_blank" rel="noopener">Core Docs</a></li>
      <li><a href="https://forum.vuejs.org" target="_blank" rel="noopener">Forum</a></li>
      <li><a href="https://chat.vuejs.org" target="_blank" rel="noopener">Community Chat</a></li>
      <li><a href="https://twitter.com/vuejs" target="_blank" rel="noopener">Twitter</a></li>
      <li><a href="https://news.vuejs.org" target="_blank" rel="noopener">News</a></li>
    </ul>
    <h3>Ecosystem</h3>
    <ul>
      <li><a href="https://router.vuejs.org" target="_blank" rel="noopener">vue-router</a></li>
      <li><a href="https://vuex.vuejs.org" target="_blank" rel="noopener">vuex</a></li>
      <li><a href="https://github.com/vuejs/vue-devtools#vue-devtools" target="_blank" rel="noopener">vue-devtools</a></li>
      <li><a href="https://vue-loader.vuejs.org" target="_blank" rel="noopener">vue-loader</a></li>
      <li><a href="https://github.com/vuejs/awesome-vue" target="_blank" rel="noopener">awesome-vue</a></li>
    </ul>-->

      <div id="myDIV" class="header">
          <h2>My To Do List</h2>
          <input type="text" id="myInput" placeholder="Title...">
          <span onclick="newElement()" class="addBtn">Add</span>
      </div>

      <ul id="myUL">
          <li>Hit the gym</li>
          <li class="checked">Pay bills</li>
          <li>Meet George</li>
          <li>Buy eggs</li>
          <li>Read a book</li>
          <li>Organize office</li>
      </ul>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
    /* Include the padding and border in an element's total width and height */
    * {
        box-sizing: border-box;
    }

    /* Remove margins and padding from the list */
    ul {
        margin: 0;
        padding: 0;
    }

    /* Style the list items */
    ul li {
        cursor: pointer;
        position: relative;
        padding: 12px 8px 12px 40px;
        background: #eee;
        font-size: 18px;
        transition: 0.2s;

        /* make the list items unselectable */
        -webkit-user-select: none;
        -moz-user-select: none;
        -ms-user-select: none;
        user-select: none;
    }

    /* Set all odd list items to a different color (zebra-stripes) */
    ul li:nth-child(odd) {
        background: #f9f9f9;
    }

    /* Darker background-color on hover */
    ul li:hover {
        background: #ddd;
    }

    /* When clicked on, add a background color and strike out text */
    ul li.checked {
        background: #888;
        color: #fff;
        text-decoration: line-through;
    }

    /* Add a "checked" mark when clicked on */
    ul li.checked::before {
        content: '';
        position: absolute;
        border-color: #fff;
        border-style: solid;
        border-width: 0 2px 2px 0;
        top: 10px;
        left: 16px;
        transform: rotate(45deg);
        height: 15px;
        width: 7px;
    }

    /* Style the close button */
    .close {
        position: absolute;
        right: 0;
        top: 0;
        padding: 12px 16px 12px 16px;
    }

    .close:hover {
        background-color: #f44336;
        color: white;
    }

    /* Style the header */
    .header {
        background-color: #f44336;
        padding: 30px 40px;
        color: white;
        text-align: center;
    }

    /* Clear floats after the header */
    .header:after {
        content: "";
        display: table;
        clear: both;
    }

    /* Style the input */
    input {
        margin: 0;
        border: none;
        border-radius: 0;
        width: 75%;
        padding: 10px;
        float: left;
        font-size: 16px;
    }

    /* Style the "Add" button */
    .addBtn {
        padding: 10px;
        width: 25%;
        background: #d9d9d9;
        color: #555;
        float: left;
        text-align: center;
        font-size: 16px;
        cursor: pointer;
        transition: 0.3s;
        border-radius: 0;
    }

    .addBtn:hover {
        background-color: #bbb;
    }
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>

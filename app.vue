<template>
    <div>
        <input type="text" v-model="newTodo" placeholder="todo"><button v-on:click="addTodo">添加</button>
        {{msg}}
        <ul>
            <li v-for="todo in todos">
                {{todo}}
            </li>
        </ul>
    </div>
</template>
<script>
export default {
  name: "app",
  data() {
    return {
      msg: "你好",
      newTodo: "ssss",
      todos: ["aaa", "bbb"]
    };
  },
  methods: {
    addTodo: function() {
      console.log("addTodo enter...");
      this.todos.push(this.newTodo);
    }
  }
};
</script>
<template>
  <div>
    <h1>Vue Todo with Typescript!</h1>
    <TodoInput :item="todoText" @input="updateTodoText" />
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import TodoInput from "./components/TodoInput.vue";

export default Vue.extend({
  components: { TodoInput },
  data() {
    return {
      todoText: "hello world!",
    };
  },
  methods: {
    addTodo() {
      console.log("add");
    },
    updateTodoText(value: any) {
      this.todoText = value;
    },
  },
});
</script>

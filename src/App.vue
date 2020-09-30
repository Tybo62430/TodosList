<template>
  <div>
    <todos v-model="todos"></todos>
    <todos v-model="todos"></todos>
    <todos></todos>
    <button @click="addTodo">Ajouter une Tâche</button>
  </div>
</template>

<script>
import Todos from "./components/Todos";

export default {
  data() {
    return {
      todos: [
        {
          name: "demo",
          completed: true,
        },
      ],
    };
  },
  components: {
    Todos,
  },
  methods: {
    addTodo() {
      this.todos.push({
        name: "Thibault",
        completed: false,
      });
    },
  },
};
</script>

<template>
  <div>
    <h1>TODO List</h1>
    <div class="todo-inputs">
      <input type="text" v-model="todoInput" />
      <button @click="addItem">Add</button>
    </div>
    <div class="todo-list">
      <div class="todo-item" v-for="(item, index) in todoList" :key="index">
        <div class="item-text">{{ item }}</div>
        <button class="item-delete-btn" @click="deleteItem(index)">
          Delete
        </button>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";

const todoInput = ref("");
const todoList = ref([]);

const addItem = () => {
  if (todoInput.value === "") return;
  todoList.value = [...todoList.value, todoInput.value];
  todoInput.value = "";
};

const deleteItem = (index) => {
  todoList.value.splice(index, 1);
};
</script>

<style scoped>
.todo-inputs {
  margin-bottom: 1em;
}

.todo-item {
  display: flex;
  justify-content: center;
}

.item-delete-btn {
  margin-left: 1em;
}
</style>

<script setup>
import { ref } from 'vue'
import Todos from './components/Todos.vue'
import Users from './components/Users.vue'
import Posts from './components/Posts.vue'

const selectedMenu = ref("todos")

const posts = ref([
  { id: 1, title: "Post 1", body: "Body 1" },
  { id: 2, title: "Post 2", body: "Body 2" },
  { id: 3, title: "Post 3", body: "Body 3" },
  { id: 4, title: "Post 4", body: "Body 4" },
  { id: 5, title: "Post 5", body: "Body 5" },
])

const users = ref([
  { id: 1, name: "User 1" },
  { id: 2, name: "User 2" },
  { id: 3, name: "User 3" },
  { id: 4, name: "User 4" },
  { id: 5, name: "User 5" },
])
</script>

<template>
  <h1>MAIN APP 2</h1>

  <button @click="selectedMenu = 'todos'">TODOS</button>
  <button @click="selectedMenu = 'posts'">POSTS</button>
  <button @click="selectedMenu = 'users'">USERS</button>
  
  <div v-if="selectedMenu == 'todos'">
    <Todos />
  </div>
  <div v-if="selectedMenu == 'posts'">
    <Posts :dataPosts="posts" />
  </div>
  <div v-if="selectedMenu == 'users'">
    <Users :users="users" />
  </div>
</template>

<style scoped>

</style>

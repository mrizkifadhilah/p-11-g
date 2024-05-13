<script setup>
import { computed, defineProps } from "vue";

const props = defineProps({
  dataPosts: Array,
});

const posts = computed(() => props.dataPosts);
</script>
<template>
  <slot name="header"></slot>

  <ul>
    <li v-for="post in posts" :key="post.id">
      <b>{{ post.title }}</b> {{ post.body }}
    </li>
  </ul>

  <slot name="footer"></slot>
</template>
<style></style>

<script setup>
const props = defineProps({
    users: Array,
})
</script>
<template>
    <h1>USERS FROM COMPONENT</h1>
    <ul>
        <li v-for="user in props.users" :key="user.id">
            {{ user.name }}
        </li>
    </ul>
</template>
<style></style>
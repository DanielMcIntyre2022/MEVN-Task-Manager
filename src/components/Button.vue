<template>
    <button @click="onClick()">Add Task</button>
</template>

<script>

export default {
    name: 'Button',
    methods: {
        onClick() {
            console.log('clicked')
        }
    }
}

</script>

<style scoped>

button {
    background-color: green;
    color: white;
    border-radius: 10%;
    padding: 10px;
    font-weight: 700;
}

</style>
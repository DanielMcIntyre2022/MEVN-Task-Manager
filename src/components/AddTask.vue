<template>
    <div class="form-container">
        <form @submit="onSubmit" class="add-form">
            <Label>Task</Label>
            <input
            type="text"
            name="text"
            placeholder="Add Task"
            v-model="text"
            />
            <button type="submit">Submit</button>
        </form>
    </div>
</template>

<script>
export default {
    name: 'AddTask',
    data() {
        return {
            text: ''
        }
    },
    methods: {
        onSubmit(e) {
            e.preventDefault()
            if(!this.text) {
                alert('Please add a task')
                return
            }

        const newTask = {
            id: Math.floor(Math.random() * 100000),
            text: this.text
        }
        this.$emit('add-task', newTask)
        }
    }
}

</script>

<style scoped>

</style>
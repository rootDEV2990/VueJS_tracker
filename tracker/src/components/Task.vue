<template>
    <div :class="[task.reminder ? 'reminder' : '', 'task']">
        <h3>
            {{ task.text }}
            <i @click="onDelete(task.id)" class="fas fa-times"></i>
        </h3>
        <p>{{ task.day }}</p>
    </div>
</template>

<script>
export default {
    name: 'Task',
    props: {
        task: Object,
    },
    methods: {
        onDelete(id) {
            this.$emit('delete-task', id)
        },
    },
}
</script>


<style scoped>
.fas {
    color: red  ;
}
.task {
    background: #f4f4f4;
    margin: .5rem;
    padding: 1rem 1.5rem;
    cursor: pointer;
}

.task.reminder {
    border-left: 5px solid green;
}

.task h3 {
    display: flex;
    justify-content: space-between;
    align-items: center;
}
</style>

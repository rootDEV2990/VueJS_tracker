<template>
    <div @dblclick="$emit('toggle-reminder', task.id)" :class="[task.reminder ? 'reminder' : '', 'task']">
        <h3>
            {{ task.text }}
            <i @click="$emit('delete-task', task.id)" class="fas fa-times"></i>
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

<template>
    <button @click="addTask()" :style="{ background: color }" class="btn">{{text}}</button>
</template>

<script>
    export default {
        name: 'Button',
        props: {
            text: String,
            color: String
        },
        methods: {
            addTask() {
                alert('Function good to go! Your code block can go here..')
            }
        }
    }
</script>

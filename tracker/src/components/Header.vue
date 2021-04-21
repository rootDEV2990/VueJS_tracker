<template>
    <header>
        <h1>{{title}}</h1>
    </header>
</template>

<script>
    export default {
        name: 'Header',
        props: {
            title: {
                type: String,
            }

        }
    } 
</script>

<style scoped>
    header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        margin-bottom: 1rem;
    }
</style>

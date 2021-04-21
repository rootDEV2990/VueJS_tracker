<template>
    <header>
        <h1>{{title}}</h1>
        <Button color="green" text="Add"/>
    </header>
</template>

<script>
    import Button from './Button'
    export default {
        name: 'Header',
        props: {
            title: {
                type: String,
            }

        },
        components: {
            Button,
        },
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

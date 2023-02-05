<script>
    export default {
        name: 'App',
        data() {
            return {
                name: 'Vishwas'
            }
            
        },
        methods: {

        },

    }

</script>

<template>
    <!-- v-once
    Renders the correcponding HTML element only once. On subsequent re-renders, the element is treated as static content and skipped -->
    <h2 v-once>{{ name }}</h2>
    <button @click="name = 'Batman'">Change name</button>

    <!-- v-pre
    Skips compilation for the correponding element
    -->
    <h2 v-pre>{{ name }}</h2>

</template>

<style>

</style>
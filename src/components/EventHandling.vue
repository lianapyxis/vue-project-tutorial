<script>

export default {
    name: 'App',
    data() {
        return {
            name: 'Vishwas',
            count: 0
        }
    },
    methods: {
        changeName(event) {
            this.name = 'Batman'
            console.log('Event', event)
        },
        increment(num, event) {
            this.count += num
            console.log('Event', event)
        },
        decrement(num) {
            this.count -= num
        },
    },
}

</script>

<template>

<h2>{{ name }}</h2>
<div>
    <button @:click="changeName($event), increment(1, $event)" >Change name</button>
    <button @:mouseover="name = 'Batman2'" >Change name</button>
</div>
<h2> {{ count }}</h2>
<div>
    <button @:click="increment(1)">Increment 1</button>
    <button @:click="increment(5)">Increment 5</button>
    <button @:click="decrement(1)">Decrement 1</button>
    <button @:click="decrement(5)">Decrement 5</button>
</div>

</template>

<style>

</style>
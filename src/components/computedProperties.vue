<script>
    export default {
        name: 'App',
        data() {
            return {
                firstName: 'Bruce',
                lastName: 'Wayne',
                items: [
                    {
                        id: 1,
                        title: 'TV',
                        price: 100,
                    },
                    {
                        id: 2,
                        title: 'Phone',
                        price: 200,
                    },
                    {
                        id:3,
                        title: 'Laptop',
                        price: 300,
                    },
                ],
            }
        },
        methods: {

        },
        computed: {
            fullName() {
                return `${this.firstName} ${this.lastName}`
            },
            total() {
                return this.items.reduce((total, current) => (total = total + current.price), 0)
            }
        }
    }

</script>

<template>
 
<h2>Full Name - {{ firstName }} {{ lastName }}</h2>
<h2>Computed Full Name - {{ fullName }}</h2>
<br>
<h2>Total - {{ items.reduce((total, current) => (total = total + current.price), 0) }}</h2>
<br>
<button @click="items.push({id: 4, title: 'Keyboard', price: 50})">Add item</button>
<h2>Computed Total - {{ total }}</h2>

</template>

<style>

</style>
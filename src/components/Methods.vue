<script>

export default {
    name: 'Methods',
    data() {
        return {
            baseMultiplier: 5,
            baseValue: 2,
        }
    },
    methods: {
        add(a, b, c) {
            return a + b + c
        },
        multiply(num) {
            return num * this.baseMultiplier
        }
    },

}

</script>

<template>

<h2>{{ 2 + 3 + 5 }}</h2>
<h2>{{ 5 + 10 + 15 }}</h2>
<h2> Add method - {{ add(2,3,5) }}</h2>
<h2> Add method - {{ add(10,15,20) }}</h2>
<h2>Multiply method - {{ multiply(baseValue) }}</h2>


</template>

<style>

</style>
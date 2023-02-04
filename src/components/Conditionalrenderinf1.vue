<script setup>

const num = 5
const display = true
const showElement = true
const names = ['Bruce', 'Clark', 'Diana']
const fullNames = [
    { first:'Bruce', last:'Wayne' },
    { first:'Clark', last:'Kent' },
    { first: 'Princess', last: 'Diana'},
]
const actors = [
    {
        name: 'Christian Bale',
        movies: ['Batman', 'The Prestige'],
    },
    {
        name: 'Di Caprio',
        movies: ['Titanic', 'Inception']
    },
]

const myInfo = {
    name: 'Vishwas',
    channel: 'Codevolution',
    course: 'Vue 3'
}

</script>

<template>

<h2 v-if="num === 0" >The number is zero</h2>
<h2 v-else-if="num < 0">The number is negative</h2>
<h2 v-else-if="num > 0">The number is positive</h2>
<h2 v-else>Not a number</h2>

<template v-if="display">
    <h2>Vishwas</h2>
    <h2>Codevolution</h2>
    <h2>Vue</h2>
</template>

<h2 v-show="showElement">Using v-show</h2> <!-- if - false display is none -->
<h2 v-if="showElement">Using v-if</h2> <!-- if false - the element is absent in the dom -->
<br>

<!--Key attribute, value, index binding-->

<h2 v-for="(name, index) in names" :key="name">{{ index }} {{ name }}</h2>
<br>
<h2 v-for="name in fullNames" :key="name.first">{{ name.first }} {{ name.last }}</h2>
<br>
<div v-for="actor in actors" :key="actor.name">
    <h2>{{ actor.name }}</h2>
    <h3 v-for="movie in actor.movies" :key="movie"> {{ movie }}</h3>
</div>
<br>
<h2 v-for="(value, key, index) in myInfo" :key="value"> {{ index }} {{ key }} : {{ value }}</h2>
<br>
<template v-for="name in names" :key="name">
    <h2>{{ name }}</h2>
    <hr />
</template>
<br>

<template v-for="name in names" :key="name" >

    <h2 v-if="name === 'Bruce'"> {{ name }}</h2> 
    
</template>


</template>

<style>

</style>
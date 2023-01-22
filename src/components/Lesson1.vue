<script setup>
import { reactive, ref } from 'vue'


const message = ref('Hello World!')

const titleClass = ref('title')

const count = ref(0)

function increment() {
  count.value++
}

const text = ref('Some text is here')

const awesome = ref(true)

function toggle() {
  awesome.value = !awesome.value
}

</script>

<template>

<br>
  <div><h1>{{ message }}</h1></div>
<br>
  <h1 v-bind:class="titleClass">Make me red</h1> <!-- add dynamic class binding here -->
  <br>
  <button @click="increment" >count is: {{ count }}</button>
  <br>
  <input v-model="text" placeholder="Type here"><br>
  <p>{{ text }}</p><br>

  <button @click="toggle">toggle</button>
  <h1 v-if="awesome">Vue is awesome!</h1>
  <h1 v-else>Oh no 😢</h1>


</template>

<style>
.title {
  color: red;
}

</style>
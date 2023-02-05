<script setup>
import { ref } from 'vue'
import ChildComp from './components/ChildComp.vue'
import Lesson1 from './components/Lesson1.vue'
import Lesson2 from './components/Lesson2.vue'
import Todoapp from './components/Todoapp.vue'
import TodoApp2 from './components/TodoApp2.vue'
import bindingelAtrrVue from './components/bindingel.atrr.vue'
import Conditionalrenderinf1 from './components/Conditionalrenderinf1.vue'
import Methods from './components/Methods.vue'
import EventHandling from './components/EventHandling.vue'
import formHandling from './components/formHandling.vue'
import bonusDirectives from './components/bonusDirectives.vue'
import computedProperties from './components/computedProperties.vue'

const greeting = ref('Hello from parent')
const childMsg = ref('No child msg yet')

</script>

<template>
<ChildComp :msg="greeting" @response="(msg) => childMsg = msg" />
<p>{{ childMsg }}</p>
<Lesson1 />
<div class="space">
<Lesson2 /></div>
<br>
<div class="space">
    <Todoapp />
</div>
<br>
<div class="space">
    <TodoApp2 />
</div>
<br>
<div class="space">
    <bindingelAtrrVue />
</div>
<br>
<div class="space">
    <Conditionalrenderinf1 />
</div>
<br>
<div class="space">
    <Methods />
</div>
<br>
<div class="space">
    <EventHandling />
</div>
<br>
<div class="space">
    <formHandling />
</div>
<br>
<div class="space">
    <bonusDirectives />
</div>
<br>
<div class="space">
    <computedProperties />
</div>

</template>

<style scoped>
.space{
    margin: 5% 0 5% 0;
}
</style>

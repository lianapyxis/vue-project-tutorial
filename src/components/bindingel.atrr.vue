<script setup>

const greet = 'Hello'
const name = 'Batman'
const channel = '<b>Codevolution</b>'
const hack = `<a href="#" onclick="alert('You have been hacked!')">Win a prize!<a/>`
const headingId = 'heading'
const isDisabled = true
const status = 'danger'
const isPromoted = true
const isSoldout = true
const hilghtlightColor = 'orange'
const headerSize = 50
const headerStyleObject = {
    color : 'orange',
    fontSize : '50px',
    padding : '20px'
}

const baseStyleObject = {
    fontSize: '50px',
    padding: '10px',
}
const successStyleObject = {
    color: 'green',
    backgroundColor: 'lightgreen',
    border: '1px solid green',
    padding: '20px',
}
const dangerStyleObject = {
    color: 'darkred',
    backgroundColor: 'red',
    border: '1px solid darkred',

}


</script>

<template>

<div>{{ greet }} {{ name }}</div>
<div v-html="channel"></div>
<div v-html="hack"></div>

<h2 v-bind:id="headingId">Heading</h2>

<button v-bind:disabled="isDisabled">Bind</button>
<h2 v-bind:class="status && 'underline'">Status</h2>
<h2 v-bind:class="isPromoted && 'promoted'">Promoted Movie</h2>
<h2 v-bind:class="isSoldout ? 'success' : 'new'">Successful movie!</h2>
<h2 v-bind:class="['new','promoted']">Newly promoted movie</h2>
<h2 v-bind:class="[isPromoted && 'promoted', isSoldout ? 'success' : 'new']">Array conditional movie</h2>

<h2 v-bind:class="{
    promoted: isPromoted,
    new: !isSoldout,
    'success' : isSoldout
}">Object conditional movie</h2>

<h2 v-bind:style="{
    color: hilghtlightColor,
    fontSize: headerSize + 'px',
    padding: '20px'
}">Inline Style</h2>

<h2 v-bind:style="headerStyleObject">Style Object</h2>

<div :style="[baseStyleObject, successStyleObject]">Succes Style</div>

<div :style="[baseStyleObject, dangerStyleObject]">Danger Style</div>



</template>

<style>
.underline{
    text-decoration: underline;
}
.danger{
    color: red;
}
.success{
    color: gold;
}
.promoted {
    font-style: italic;
}
.new{
    color: green;
}
</style>
<script setup>
import {reactive} from 'vue'
import ChildComponent from './components./ChildComponent.vue';
const persons=reactive({
    name:'Md Safiqul Islam',
    age : 25,
    occupation : 'web developer',
    message : 'Hi,I am a  new web Developer'
})
</script>
<template>
    <div class="mt-10 ">
        <h1 class="my-5">Parent Component</h1>
        <h2 class="text-l">Name: {{persons.name}}</h2>
        <h2 class="text-l">Age :{{persons.age}}</h2>
        <p class="text-l">Occupation :{{persons.occupation}}</p>
        <p class="text-l">Message :{{persons.message}}</p>

    </div>

    <ChildComponent v-model:message="persons.message"/>
</template>
<style scoped></style>

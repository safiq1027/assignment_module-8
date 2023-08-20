<script setup>
const props = defineProps(['message']);
const emit = defineEmits(['update:modlValue']);

function messageEmitted(){
    props.name=emit('update:message','hi,I am a new Vue js3 Learner !!')
}
</script>
<template>
    <div class="mt-10">
        <h1 class="text-2xl my-5"> Child Component</h1>
        <p class="text-xl my-5"> Message :{{ message }}</p>

        <button @click="messageEmitted()" class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">
            Button
        </button>

    </div>

</template>
<style scoped></style>
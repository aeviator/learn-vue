<script setup>
    import { ref } from 'vue'
    import { reactive } from 'vue'

    const counter = reactive({
        count: 0
    })

    console.log(counter.count)
    counter.count++
    
    const titleClass = ref('title')

    const message = ref ('Hello World!')
    const message_d = ref('Make me Dynamic')
    console.log(message.value)
    console.log(message_d.value)
    message.value = 'Changed'
    message_d.value = 'I am Dynamic'
</script>

<template>
    <h1>Make me Dynamic</h1>
    <h1>{{ message_d.split('').reverse('').join('') }}</h1>
    <h1>Change</h1>
    <h1>{{ message.split('').reverse('').join('') }}</h1>
    <h1>{{ message.split('') }}</h1>
    <h1>{{ message.split('').reverse('') }}</h1>

    <h1>Make me Red</h1>
    <h1 :class='titleClass'>{{ ('I am Red').split('').reverse('').join('') }}</h1>
</template>

<style>
.title {
  color: red;
}
</style>

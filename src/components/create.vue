<template>
    <div>
        <h1>{{ title }}</h1>
        <form @submit.prevent="add">
            <input type="text" v-model="state.addInput">
            <button type="submit">Add</button>
        </form>
    </div>
</template>

<script setup>
    import { reactive } from 'vue';
    const state = reactive({
        addInput: ''
    });
    const props = defineProps({
        title: String
    })
    const emit = defineEmits(['submit'])
    function add() {
        emit('submit', state.addInput)
        state.addInput = ''
    }
</script>

<style scoped>
    input {
        width: 155px;
        border-top-left-radius: 11px;
        border-bottom-left-radius: 11px;
    }
</style>
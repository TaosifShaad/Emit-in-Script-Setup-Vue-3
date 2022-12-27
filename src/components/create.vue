<template>
    <div>
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
    const emit = defineEmits(['submit'])
    function add() {
        emit('submit', state.addInput)
        // state.addInput = ''
    }
</script>

<style scoped>

</style>
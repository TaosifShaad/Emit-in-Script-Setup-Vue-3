<template>
    <div>
        <li v-for="item in state.items"> {{ item }} </li>
    </div>
    <create @submit="add"></create>
</template>


<script setup>
    import create from '@/components/create.vue';
    import { reactive } from 'vue';
    const state = reactive({
        items: [
            'item 1',
            'item 2',
            'item 3'
        ]
    })
    function add(e) {
        console.log(e)
        state.items.push(e);
    }
</script>


<style lang="scss" scoped>

</style>
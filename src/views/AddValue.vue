<template>
    <div id="all">
        <div class="items">
            <li v-for="item in state.items"> {{ item }} </li>
        </div>
        <create :title="state.title" @submit="add"></create>
    </div> 
</template>


<script setup>
    import create from '@/components/create.vue';
    import { reactive } from 'vue';
    const state = reactive({
        title: 'Add Items:',
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


<style scoped>
    #all {
        border-radius: 64px;
        background: #ffffff;
        box-shadow: 0px 0px 11px #878787, -19px 19px 38px #ffffff;
        width: 45%;
        height: 99%;
        padding: 35px;
        margin-left: 200px;
    }
    .items {
        list-style: none;
        border: 1px solid;
        max-width: 96%;
        text-align: center;
        border-radius: 17px;
        box-shadow: 0px 0px 9px 5px navajowhite;
    }
    li {
        border-bottom: 1px solid;
        border-radius: 20px;
    }
</style>
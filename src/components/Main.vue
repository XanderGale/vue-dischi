<template>
    <main>
        <div class="container">
            <div class="items-list">
                <SingleItem v-for="(item, index) in itemsList" :key="index" :itemDetails="item"/>
            </div>
        </div>
    </main>
</template>

<script>
import axios from 'axios';

import SingleItem from './SingleItem.vue';

export default {
    name: 'Mail',
    components: {
        SingleItem,
    },
    data: function(){
        return {
            itemsList: [],
        }
    },
    methods: {
        loadItems: function(){
            axios.get('https://flynn.boolean.careers/exercises/api/array/music')
            .then ((answer) => {
                this.itemsList = answer.data.response;
            });
        }
    },
    created: function(){
        this.loadItems();
    }
}
</script>

<style scoped lang="scss">
    main{
        height: calc(100% - 50px);
        width: 100%;
        padding: 50px 0;
        .items-list{
            display: flex;
            flex-flow: row wrap;
            justify-content: flex-start;
            align-items: flex-start;
        }
    }
</style>
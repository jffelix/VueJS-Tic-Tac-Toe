<template>
    <main>
        <div 
            className='rowA1' 
            v-on:click="this.markBox">{{this.boxA1}}</div>
    </main>
</template>

<script>
export default {
    name: 'RowA1',
    props: {
        boxA1: String,
        currentPlayer: String
    },
    methods: {
        markBox() {
            console.log('A1');
            this.$emit('changePlayer');
            this.$emit('markA1')
        }
    },
    emits: ['changePlayer', 'markA1']
}
</script>

<style>
.rowA1 {
    border-style: solid;
    width: 125px;
    height: 125px;
}

</style>
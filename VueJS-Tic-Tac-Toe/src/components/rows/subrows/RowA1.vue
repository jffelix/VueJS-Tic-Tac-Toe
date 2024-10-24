<template>
    <main>
        <div 
            className='rowA1' 
            v-on:click="this.markBoxA1">{{this.boxA1}}</div>
    </main>
</template>

<script>
export default {
    name: 'RowA1',
    data() {
        return {
            wasSelected: false
        }
    },
    props: {
        boxA1: String,
        currentPlayer: String
    },
    methods: {
        markBoxA1() {
            if (this.wasSelected === false) {
                this.$emit('changePlayer');
                this.$emit('markA1')
                this.wasSelected = !this.wasSelected
            }
            console.log('A1');
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
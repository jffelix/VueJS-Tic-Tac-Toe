<template>
    <main>
        <div 
            className='rowA1' 
            v-on:click="this.markBoxA1">
            <h3>{{this.boxA1}}</h3>
        </div>
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
        }
    },
    emits: ['changePlayer', 'markA1']
}
</script>

<style>
.rowA1 {
    display: flex;
    flex-direction: column;
    justify-content: center;
    text-align: center;
    border-style: solid;
    width: 125px;
    height: 125px;
}

</style>
<template>
    <main>
        <div 
            className='rowB1'
            v-on:click="this.markBoxB1"
        >
            <h3>{{this.boxB1}}</h3>
        </div>
    </main>
</template>

<script>
export default {
    name: 'RowB1',
    data() {
        return {
            wasSelectedB1: false
        }
    },
    props: {
        boxB1: String,
        currentPlayer: String
    },
    emits: ["changePlayerRowB", "markB1"],
    methods: {
        markBoxB1() {
            if (this.wasSelectedB1 === false) {
                this.$emit("changePlayerRowB")
                this.$emit("markB1")
                this.wasSelectedB1 = !this.wasSelectedB1
            }
        }
    }
}

</script>

<style>

.rowB1 {
    display: flex;
    flex-direction: column;
    justify-content: center;
    text-align: center;
    border-style: solid;
    width: 125px;
    height: 125px;
}

</style>
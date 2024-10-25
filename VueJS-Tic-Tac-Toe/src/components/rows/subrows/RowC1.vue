<template>
    <main 
        className='rowC1'
        v-on:click="this.markBoxC1"
    >
        <h3>{{this.rowC1}}</h3>
    </main>
</template>

<script>
export default {
    name: 'RowC1',
    data() {
        return {
            wasSelectedC1: false
        }
    },
    props: {
        rowC1: String
    },
    emits: ["changePlayerRowC", "markC1"],
    methods: {
        markBoxC1() {
            if (this.wasSelectedC1 === false) {
                this.$emit("changePlayerRowC")
                this.$emit("markC1")
                this.wasSelectedC1 = !this.wasSelectedC1
            }
        }
    }
}
</script>

<style>
.rowC1 {
    border-style: solid;
    width: 125px;
    height: 125px;
}
</style>
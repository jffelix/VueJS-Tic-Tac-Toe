<template>
    <main 
        className='boxC1'
        v-on:click="this.markBoxC1"
    >
        <h3>{{this.boxC1}}</h3>
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
        boxC1: String
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
.boxC1 {
    display: flex;
    flex-direction: column;
    justify-content: center;
    text-align: center;
    border-style: solid;
    width: 125px;
    height: 125px;
}

.boxC1 h3 {
    /* margin: auto;
    text-align: center; */
    /* display: flex;
    justify-content: center; */
}
</style>
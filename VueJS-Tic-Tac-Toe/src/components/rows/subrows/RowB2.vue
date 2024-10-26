<template>
    <main>
        <div 
            className='rowB2'
            v-on:click="this.markBoxB2"
        >
            <h3>{{this.boxB2}}</h3>
        </div>
    </main>
</template>

<script>
export default {
    name: "RowB2",
    data() {
        return {
            wasSelectedB2: false
        }
    },
    props: {
        boxB2: String
    },
    emits: ["changePlayerRowB", "markB2"],
    methods: {
        markBoxB2() {
            if (this.wasSelectedB2 === false) {
                this.$emit("changePlayerRowB")
                this.$emit("markB2")
                this.wasSelectedB2 = !this.wasSelectedB2
            }
        }
    }
}
</script>

<style>
.rowB2 {
    display: flex;
    flex-direction: column;
    justify-content: center;
    text-align: center;
    border-style: solid;
    width: 125px;
    height: 125px;
}
</style>
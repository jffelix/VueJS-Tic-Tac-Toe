<template>
    <main>
        <div 
            className='rowC2'
            v-on:click="this.markBoxC2"
        >
            <h3>{{this.rowC2}}</h3>
        </div>
    </main>
</template>

<script>
export default {
    name: 'RowC2',
    data() {
        return {
            wasSelectedC2: false
        }
    },
    props: {
        rowC2: String
    },
    emits: ["changePlayerRowC", "markC2"],
    methods: {
        markBoxC2() {
            if (this.wasSelectedC2 === false) {
                this.$emit("changePlayerRowC")
                this.$emit("markC2")
                this.wasSelectedC2 = !this.wasSelectedC2
            }
        }
    }
}
</script>

<style>
.rowC2 {
    border-style: solid;
    width: 125px;
    height: 125px;
}
</style>
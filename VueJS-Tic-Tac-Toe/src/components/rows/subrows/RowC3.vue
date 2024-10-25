<template>
    <main>
        <div 
            className='rowC3'
            v-on:click="this.markBoxC3"
        >
            <h3>{{this.rowC3}}</h3>
        </div>
    </main>
</template>

<script>
export default {
    name: 'RowC3',
    data() {
        return {
            wasSelectedC3: false
        }
    },
    props: {
        rowC3: String
    },
    emits: ["changePlayerRowC", "markC3"],
    methods: {
        markBoxC3() {
            if (this.wasSelectedC3 === false) {
                this.$emit("changePlayerRowC")
                this.$emit("markC3")
                this.wasSelectedC3 = !this.wasSelectedC3
            }
        }
    }
}
</script>

<style>
.rowC3 {
    border-style: solid;
    width: 125px;
    height: 125px;
}
</style>
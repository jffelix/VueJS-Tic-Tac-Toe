<template>
    <main>
        <div 
            className='rowA3'
            v-on:click="this.markBoxA3">
            <h3>{{this.boxA3}}</h3>
        </div>
    </main>
</template>

<script>
export default {
    name: 'RowA3',
    data() {
        return {
            wasSelectedA3: false
        }
    },
    props: {
        currentPlayer: String,
        boxA3: String
    },
    emits: ["changePlayer", "markA3"],
    methods: {
        markBoxA3() {
            if (this.wasSelectedA3 === false) {
                this.$emit("changePlayer"),
                this.$emit("markA3")
                this.wasSelectedA3 = !this.wasSelectedA3
            }
        }
    }
}
</script>

<style>
.rowA3 {
    border-style: solid;
    width: 125px;
    height: 125px;
}

</style>
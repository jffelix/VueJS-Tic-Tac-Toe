<template>
    <main>
        <div 
            className='rowA2'
            v-on:click="this.markBoxA2">
            <h3>{{this.boxA2}}</h3>
        </div>
    </main>
</template>

<script>
export default {
    name: 'RowA2',
    data() {
        return {
            alreadySelectedA2: false
        }
    },
    props: {
        currentPlayer: String,
        boxA2: String
    },
    emits: ["changePlayer", "markA2"],
    methods: {
        markBoxA2() {
            if (this.alreadySelectedA2 === false) {
                this.$emit("changePlayer")
                this.$emit("markA2")
                this.alreadySelectedA2 = !this.alreadySelectedA2
            }
        }
    }
}
</script>

<style>
.rowA2 {
    display: flex;
    flex-direction: column;
    justify-content: center;
    text-align: center;
    border-style: solid;
    width: 125px;
    height: 125px;
}

</style>
<template>
    <main>
        <div 
            className='rowB3'
            v-on:click="this.markBoxB3"    
        >
            <h3>{{this.boxB3}}</h3>
        </div>
    </main>
</template>

<script>
export default {
    name: "RowB3",
    data() {
        return {
            wasSelelctedB3: false
        }
    },
    props: {
        boxB3: String
    },
    emits: ["changePlayerRowB", "markB3"],
    methods: {
        markBoxB3() {
            if (this.wasSelelctedB3 === false) {
                this.$emit("changePlayerRowB")
                this.$emit("markB3")
                this.wasSelelctedB3 = !this.wasSelelctedB3
            }
        }
    }
}
</script>

<style>
.rowB3 {
    border-style: solid;
    width: 125px;
    height: 125px;
}
</style>
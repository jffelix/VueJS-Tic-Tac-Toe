<template>
    <main>
        <div className='rowA1' v-on:click="this.markBox"></div>
    </main>
</template>

<script>
export default {
    name: 'RowA1',
    methods: {
        markBox() {
            console.log('A1');
            this.$emit('changePlayer');
        }
    },
    emits: ['changePlayer']
}
</script>

<style>
.rowA1 {
    border-style: solid;
    width: 125px;
    height: 125px;
}

</style>
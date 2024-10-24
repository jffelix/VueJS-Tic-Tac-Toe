<template>
  <header>
  </header>

  <main>
    <div className='firstRow'>
        <RowA1 v-on:changePlayer="changePlayer"/>
        <RowA2 />
        <RowA3 />
    </div>
  </main>
</template>

<script>
import RowA1 from './subrows/RowA1.vue'
import RowA2 from './subrows/RowA2.vue'
import RowA3 from './subrows/RowA3.vue'

export default {
    name: 'TopRow',
    components: {
        RowA1,
        RowA2,
        RowA3
    },
    emits: ['changePlayer'],
    methods: {
        changePlayer() {
            this.$emit("changePlayer")
        }
    }
}

</script>

<style>
.firstRow {
    display: flex;
    flex-direction: row;
}
</style>

<template>
  <header>
  </header>

  <main>
    <div className='firstRow'>
        <RowA1 
            v-on:changePlayer="changePlayer"
            v-on:markA1="markA1"
            :currentPlayer="this.currentPlayer"
            :boxA1="this.boxA1"
        />
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
    props: {
        currentPlayer: String
    },
    components: {
        RowA1,
        RowA2,
        RowA3
    },
    data() {
        return {
            boxA1: null
        }
    },
    // created() {
    //     this.fullRowA = {
    //         boxA1: null
    //     }
    // },
    emits: ['changePlayer'],
    methods: {
        changePlayer() {
            this.$emit("changePlayer")
        },
        markA1() {
            this.boxA1 = this.currentPlayer
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

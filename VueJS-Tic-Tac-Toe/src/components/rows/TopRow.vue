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
        <RowA2
            v-on:changePlayer="changePlayer" 
            v-on:markA2="markA2"
            :currentPlayer="this.currentPlayer"
            :boxA2="this.boxA2"
        />
        <RowA3 
            v-on:changePlayer="changePlayer"
            v-on:markA3="markA3"
            :currentPlayer="this.currentPlayer"
            :boxA3="this.boxA3"
        />
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
            boxA1: null,
            boxA2: null,
            boxA3: null
        }
    },
    emits: ['changePlayer'],
    methods: {
        changePlayer() {
            this.$emit("changePlayer")
        },
        markA1() {
            this.boxA1 = this.currentPlayer
        },
        markA2() {
            this.boxA2 = this.currentPlayer
        },
        markA3() {
            this.boxA3 = this.currentPlayer
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

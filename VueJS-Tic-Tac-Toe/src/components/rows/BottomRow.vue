<template>
  <header>
  </header>

  <main>
    <div className='thirdRow'>
      <RowC1 
        v-on:changePlayerRowC="changePlayerRowC"
        v-on:markC1="markC1"
        :boxC1="this.boxC1"
      />
      <RowC2 
        v-on:changePlayerRowC="changePlayerRowC"
        v-on:markC2="markC2"
        :boxC2="this.boxC2"
      />
      <RowC3 
        v-on:changePlayerRowC="changePlayerRowC"
        v-on:markC3="markC3"
        :rowC3="this.rowC3"
      />
    </div>
  </main>
</template>

<script>
import RowC1 from './subrows/RowC1.vue'
import RowC2 from './subrows/RowC2.vue'
import RowC3 from './subrows/RowC3.vue'

export default {
    name: 'BottomRow',
    components: {
      RowC1,
      RowC2,
      RowC3
    },
    data() {
      return {
        boxC1: null,
        boxC2: null,
        rowC3: null
      }
    },
    props: {
      currentPlayer: String
    },
    emits: ["changePlayer"],
    methods: {
      changePlayerRowC() {
        this.$emit("changePlayer")
      },
      markC1() {
        this.boxC1 = this.currentPlayer
      },
      markC2() {
        this.boxC2 = this.currentPlayer
      },
      markC3() {
        this.rowC3 = this.currentPlayer
      }
    }
}

</script>

<style>
.thirdRow {
    display: flex;
    flex-direction: row;
}
</style>

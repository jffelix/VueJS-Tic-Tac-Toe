<template>
  <header>
  </header>

  <main>
    <div className='secondRow'>
      <RowB1 
        v-on:changePlayerRowB="changePlayerRowB"
        v-on:markB1="markB1"
        :boxB1="this.boxB1"
        :currentPlayer="currentPlayer"
      />
      <RowB2 
        v-on:changePlayerRowB="changePlayerRowB"
        v-on:markB2="markB2"
        :boxB2="this.boxB2"
      />
      <RowB3 />
    </div>
  </main>
</template>

<script>
import RowB1 from './subrows/RowB1.vue'
import RowB2 from './subrows/RowB2.vue'
import RowB3 from './subrows/RowB3.vue'

export default {
    name: 'MiddleRow',
    components: {
      RowB1,
      RowB2,
      RowB3
    },
    data() {
      return {
        boxB1: null,
        boxB2: null
      }
    },
    props: {
      currentPlayer: String
    },
    emits: ["changePlayer"],
    methods: {
      changePlayerRowB() {
        this.$emit("changePlayer")
      },
      markB1() {
        this.boxB1 = this.currentPlayer
      },
      markB2() {
        this.boxB2 = this.currentPlayer
      }
    }
}

</script>

<style>
.secondRow {
    display: flex;
    flex-direction: row;
}
</style>

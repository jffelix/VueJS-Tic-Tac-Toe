<template>
  <header>
  </header>

  <main>
    <div>
      <div className='title'>
        <h1>VueJS Tic-Tac-Toe</h1>
      </div>
      <div>Current Player: {{this.currentPlayer}}</div>
      <div className='allRows'>
        <TopRow 
          v-on:changePlayer="changePlayer"
          :currentPlayer="this.currentPlayer"  
        />
        <MiddleRow 
          v-on:changePlayer="changePlayer"
          :currentPlayer="this.currentPlayer"
        />
        <BottomRow 
          v-on:changePlayer="changePlayer"
          :currentPlayer="this.currentPlayer"
        />
      </div>
    </div>
  </main>
</template>

<script>
import TopRow from './rows/TopRow.vue'
import MiddleRow from './rows/MiddleRow.vue'
import BottomRow from './rows/BottomRow.vue'

export default {
  name: 'App',
  components: {
    TopRow,
    MiddleRow,
    BottomRow
  },
  data() {
    return {
      currentPlayer: 'X'
    }
  },
  methods: {
    changePlayer() {
      if (this.currentPlayer === 'X') {
        this.currentPlayer = '0';
      } else {
        this.currentPlayer = 'X'
      }
    }
  }
}
</script>

<style>

</style>

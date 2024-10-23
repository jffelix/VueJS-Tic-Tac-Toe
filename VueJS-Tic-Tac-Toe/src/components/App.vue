<template>
  <header>
  </header>

  <main>
    <div className='title'>
      <h1>VueJS Tic-Tac-Toe</h1>
    </div>
    <div>
      <TopRow />
      <MiddleRow />
      <BottomRow />
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
  }
}
</script>

<style>

</style>

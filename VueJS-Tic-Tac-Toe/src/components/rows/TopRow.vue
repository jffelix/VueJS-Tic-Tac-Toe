<template>
  <header>
  </header>

  <main>
    <div className='topRow'>
        <h2>Top Row</h2>
        <RowA1 />
        <RowA2 />
    </div>
  </main>
</template>

<script>
import RowA1 from './subrows/RowA1.vue'
import RowA2 from './subrows/RowA2.vue'

export default {
    name: 'TopRow',
    components: {
        RowA1,
        RowA2
    }
}

</script>

<style>

</style>

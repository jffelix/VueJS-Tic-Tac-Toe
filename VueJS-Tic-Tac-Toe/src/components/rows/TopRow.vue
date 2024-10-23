<template>
  <header>
  </header>

  <main>
    <div className='topRow'>
        <h2>Top Row</h2>
        <RowA1 />
    </div>
  </main>
</template>

<script>
import RowA1 from './subrows/RowA1.vue'

export default {
    name: 'TopRow',
    components: {
        RowA1
    }
}

</script>

<style>

</style>

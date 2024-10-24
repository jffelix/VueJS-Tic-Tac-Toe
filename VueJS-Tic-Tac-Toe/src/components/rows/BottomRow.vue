<template>
  <header>
  </header>

  <main>
    <div className='thirdRow'>
      <h2>Bottom Row</h2>
      <RowC1 />
      <RowC2 />
      <RowC3 />
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
    }
}

</script>

<style>

</style>

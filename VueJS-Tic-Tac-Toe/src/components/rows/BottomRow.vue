<template>
  <header>
  </header>

  <main>
    <div>
      <h2>Bottom Row</h2>
      <RowC1 />
      <RowC2 />
    </div>
  </main>
</template>

<script>
import RowC1 from './subrows/RowC1.vue'
import RowC2 from './subrows/RowC2.vue'

export default {
    name: 'BottomRow',
    components: {
      RowC1,
      RowC2
    }
}

</script>

<style>

</style>

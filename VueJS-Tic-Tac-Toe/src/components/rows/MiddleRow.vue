<template>
  <header>
  </header>

  <main>
    <div>
      <h2>Middle Row</h2>
      <RowB1 />
      <RowB2 />
    </div>
  </main>
</template>

<script>
import RowB1 from './subrows/RowB1.vue'
import RowB2 from './subrows/RowB2.vue'

export default {
    name: 'MiddleRow',
    components: {
      RowB1,
      RowB2
    }
}

</script>

<style>
</style>

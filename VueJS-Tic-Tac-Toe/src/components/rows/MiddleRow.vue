<template>
  <header>
  </header>

  <main>
    <div>
      <h2>Middle Row</h2>
      <RowB1 />
    </div>
  </main>
</template>

<script>
import RowB1 from './subrows/RowB1.vue'

export default {
    name: 'MiddleRow',
    components: {
      RowB1
    }
}

</script>

<style>
</style>

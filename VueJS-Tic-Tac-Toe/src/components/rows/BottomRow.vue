<template>
  <header>
  </header>

  <main>
    <div>
      <h2>Bottom Row</h2>
      <RowC1 />
    </div>
  </main>
</template>

<script>
import RowC1 from './subrows/RowC1.vue'

export default {
    name: 'BottomRow',
    components: {
      RowC1
    }
}

</script>

<style>

</style>

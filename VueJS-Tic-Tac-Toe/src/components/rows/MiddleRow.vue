<template>
  <header>
  </header>

  <main>
    <div className='secondRow'>
      <RowB1 />
      <RowB2 />
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
    }
}

</script>

<style>
.secondRow {
    display: flex;
    flex-direction: row;
}
</style>

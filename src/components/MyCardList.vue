<template>
  <HorizontalScroll class="my-card-list hide-horizontal-scrollbar">
    <MyCard v-for="card in section" :key="card.index" :card="card" />
  </HorizontalScroll>
</template>

<script>
import MyCard from './MyCard';
import HorizontalScroll from 'vue-horizontal-scroll';
import 'vue-horizontal-scroll/dist/vue-horizontal-scroll.css';
export default {
  name: 'my-card-list',
  components: { MyCard, HorizontalScroll },
  props: {
    section: {
      type: Array,
      default: () => [],
    },
  },
};
</script>

<style lang="scss">
.my-card-list {
  display: flex;
  align-items: stretch;
}
</style>

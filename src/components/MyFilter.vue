<template>
  <horizontal-scroll
    class="my-filter hide-horizontal-scrollbar"
    :class="{ 'is-hidden': !isShowNavbar }"
  >
    <MyFilterItem v-for="block in blocks" :key="block.id" :block="block" />
  </horizontal-scroll>
</template>

<script>
import MyFilterItem from './MyFilterItem';
import HorizontalScroll from 'vue-horizontal-scroll';
import 'vue-horizontal-scroll/dist/vue-horizontal-scroll.css';
export default {
  name: 'my-filter',
  components: {
    MyFilterItem,
    HorizontalScroll,
  },
  props: {
    blocks: {
      type: Array,
      default: () => [],
    },
    isShowNavbar: {
      type: Boolean,
    },
  },
};
</script>

<style lang="scss">
.my-filter {
  display: flex;
  align-items: center;
  margin-top: 15px;
  transform: translate3d(0, 0, 0);
  transition: 0.01s all ease-out;
  &.is-hidden {
    margin-top: 0;
    transform: translate3d(0, 40%, 0);
    max-height: 0;
  }
}
</style>

<template>
  <header id="my-header" class="my-header">
    <MySearch />
    <transition name="fade"
      ><MyFilter :isShowNavbar="isShowNavbar" :blocks="blocks"
    /></transition>
  </header>
</template>

<script>
import MyFilter from './MyFilter';
import MySearch from './MySearch';
export default {
  name: 'my-header',
  components: {
    MyFilter,
    MySearch,
  },
  props: {
    blocks: {
      type: Array,
      default: () => [],
    },
  },
  data() {
    return {
      isShowNavbar: true,
      lastScrollPosition: 0,
      scrollValue: 0,
      offset: 5,
    };
  },
  methods: {
    handleScroll() {
      if (window.pageYOffset < 0) {
        return;
      }
      if (
        Math.abs(window.pageYOffset - this.lastScrollPosition) < this.offset
      ) {
        return;
      }
      this.isShowNavbar = window.pageYOffset < this.lastScrollPosition;
      this.lastScrollPosition = window.pageYOffset;
    },
  },
  mounted() {
    this.lastScrollPosition = window.pageYOffset;
    window.addEventListener('scroll', this.handleScroll);
  },
  beforeDestroy() {
    window.removeEventListener('scroll', this.handleScroll);
  },
};
</script>

<style lang="scss">
.my-header {
  padding: 10px 10px 20px;
  background: #fff;
  position: fixed;
  top: 0;
  width: 100%;
  z-index: 2;
}
.fade-enter-active,
.fade-leave-active {
  transition: 0s all ease-out;
}

.fade-enter,
.fade-leave-to {
  opacity: 0;
}
</style>

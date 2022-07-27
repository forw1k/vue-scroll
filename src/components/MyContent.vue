<template>
  <div class="my-content" :style="{ 'padding-top': headerHeight + 'px' }">
    <div
      v-for="section in sections"
      :key="section.index"
      class="my-content__item"
    >
      <div class="my-head">
        <div class="my-title">{{ section.header }}</div>
        <a href="#" class="my-link">Смотреть все ></a>
      </div>
      <MyCardList :section="section.section" />
    </div>
  </div>
</template>

<script>
import MyCardList from './MyCardList';
export default {
  name: 'my-content',
  components: { MyCardList },
  props: {
    sections: {
      type: Array,
      default: () => [],
    },
    headerHeight: {
      type: Number,
    },
  },
};
</script>

<style lang="scss">
.my-head {
  display: flex;
  align-items: flex-start;
  justify-content: space-between;
}
.my-title {
  margin-bottom: 20px;
  font-weight: bold;
}
.my-link {
  text-decoration: none;
  color: rgb(77, 185, 185);
  padding-right: 5px;
}
.my-content {
  padding: 0 0 0 10px;
  &__item {
    margin-bottom: 30px;
  }
}
</style>

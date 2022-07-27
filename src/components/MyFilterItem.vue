<template>
  <div class="my-filter-item">
    <img :src="block.src" class="my-filter-item__icon" alt="filter icon" />
    <div>{{ block.name }}</div>
  </div>
</template>

<script>
export default {
  name: 'my-filter-item',
  props: {
    block: {
      type: Object,
      default: () => {},
    },
  },
};
</script>

<style lang="scss">
.my-filter-item {
  display: flex;
  align-items: center;
  width: fit-content;
  color: #ccc;
  border: 2px solid #ccc;
  border-radius: 5px;
  padding: 5px 10px;
  margin-right: 15px;
  white-space: nowrap;
  &:hover {
    cursor: pointer;
  }
  &__icon {
    width: 16px;
    margin-right: 10px;
  }
}
</style>

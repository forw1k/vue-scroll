<template>
  <div class="my-search">
    <input
      type="text"
      class="my-search__input"
      placeholder="Поиск по всем категориям"
    />
    <img
      src="magnifying-glass-solid.svg"
      class="my-search__icon"
      alt="search btn"
    />
  </div>
</template>

<script>
export default {
  name: 'my-search',
};
</script>

<style lang="scss">
.my-search {
  position: relative;
  &__input {
    width: 100%;
    padding: 10px;
    background: #f5f5f5;
    border-radius: 10px;
    border: none;
    transition: 0.25s;
    &:focus {
      outline: none;
      box-shadow: 0 0 6px rgba(0, 0, 0, 0.5);
    }
  }
  &__icon {
    width: 16px;
    position: absolute;
    right: 2%;
    top: 30%;
  }
}
</style>

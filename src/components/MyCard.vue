<template>
  <div class="my-card">
    <div class="my-card__img">
      <img :src="card.src" class="my-card__pic" alt="image" />
    </div>
    <div class="my-card__info">
      <div class="my-card__slogan">{{ card.slogan }}</div>
      <div class="my-card__brand">{{ card.brand }}</div>
      <div class="my-card__adress">
        <span class="my-card__desc">Ближайшее: </span>
        {{ card.adress }}
      </div>
    </div>
    <div class="my-card__promotion">{{ card.promotion }}</div>
  </div>
</template>

<script>
export default {
  name: 'my-card',
  props: {
    card: {
      type: Object,
      default: () => {},
    },
  },
};
</script>

<style lang="scss">
.my-card {
  position: relative;
  display: flex;
  flex-direction: column;
  width: 70%;
  flex-shrink: 0;
  margin-right: 10px;
  white-space: normal;
  &__img {
    width: 100%;
    height: 200px;
    border-radius: 10px;
    overflow: hidden;
  }
  &__pic {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }
  &__info {
    height: 200px;
    padding: 10px;
    background: #fff;
  }
  &__slogan {
    margin-bottom: 20px;
    font-weight: bold;
  }
  &__brand {
    margin-bottom: 10px;
    font-weight: bold;
  }
  &__adress {
    color: grey;
    font-weight: bold;
  }
  &__desc {
    font-weight: normal;
  }
  &__promotion {
    position: absolute;
    top: 0;
    left: 10%;
    background: rgb(207, 78, 78);
    color: #fff;
    padding: 5px;
  }
}
</style>

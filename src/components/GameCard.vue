<template>
  <div class="game-card">
    <div class="game-card__img">
      <img :src="gameInfo.thumbnailImageUrl" alt="img">
    </div>
    <div class="game-card__info">
      <div class="game-card__head">
        <div class="game-card__head-left">
          <p class="game-card__title">{{ gameInfo.name }}</p>
          <p class="game-card__action">#Action</p>
        </div>

        <div class="game-card__head-price">${{ gameInfo.rate }}</div>
      </div>

      <p class="game-card__description">
        {{ gameInfo.description }}
      </p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    gameInfo: {
      type: Object,
      required: true,
    }
  },

  setup() {
    
  },
}
</script>

<style lang="scss" scoped>
.game-card {
  border-radius: 20px;
  overflow: hidden;
  background-color: #292f45;
  &__img {
    height: 0;
    img {
      width: 100%;
      height: 300px;
      object-fit: cover;
      border-radius: 20px;
    }
  }
  &__info {
    padding: 20px;
    padding-top: 310px;
  }
  &__head {
    display: flex;
    align-items: center;
    justify-content: space-between;
    &-price {
      background-color: #5e6373;
      color: white;
      padding: 4px;
      border-radius: 50px;
      min-width: 30px;
      text-align: center;
      font-size: 18px;
      font-weight: 700;
    }
  }
  &__title {
    font-size: 18px;
    margin: 0;
    color: white;
    font-weight: 700;
  }
  &__action {
    margin: 0;
    color: #8f628f;
    font-weight: 700;
  }
}
</style>
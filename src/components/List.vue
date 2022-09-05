<template>
  <div class="list">
    <div class="list__title">{{ title }}</div>

    <div class="list__wrapper">
      <slot />
    </div>

    <div class="list__bottom">
      <button class="list__bottom--view-more">VIEW MORE</button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ItemList',

  props: {
    title: {
      type: String,
      default: ''
    }
  },

  setup() {
    
  },
}
</script>

<style lang="scss" scoped>
.list {
  &__title {
    color: white;
    font-size: 16px;
    font-weight: 700;
    margin-bottom: 20px;
  }
  &__wrapper {
    display: grid;
    gap: 24px;
    grid-template-columns: 1fr 1fr 1fr;
  }
  &__bottom {
    display: flex;
    justify-content: flex-end;
    &--view-more {
      cursor: pointer;
      border: 1px solid white;
      background-color: transparent;
      border-radius: 20px;
      color: white;
      font-weight: 600;
      padding: 6px;
      margin-top: 20px;
    }
  }
}
</style>
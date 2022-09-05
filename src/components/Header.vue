<template>
  <div class="header">
    <div class="header__left">
      <span class="header__left--logo">GAMEJAM</span>
      <a href="#" class="header__link">BROWSE GAMES</a>
    </div>

    <div class="header__center">
      <a href="#" class="header__link">UPLOAD GAMES</a>
      <a href="#" class="header__link">COMMUNITY</a>
      <a href="#" class="header__link">SUPPORT</a>
    </div>

    <div class="header__right">
      <a href="#" class="header__link">Sign up</a>
      <a href="#" class="header__link">Log in</a>
    </div>
  </div>
</template>

<script>
export default {
  name: 'MyHeader',
  setup() {
    
  },
}
</script>

<style lang="scss" scoped>
.header {
  display: flex;
  padding: 32px;
  background-color: #272c40;
  color: white;
  justify-content: space-between;
  align-items: center;
  > * {
    display: flex;
  }
  &__left {
    align-items: center;
    gap: 32px;

    &--logo {
      font-size: 32px;
      font-weight: 700;
    }
  }
  &__center {
    justify-content: space-between;
    min-width: 500px;
  }
  &__right {
    gap: 32px;
  }
  &__link {
    color: white;
    text-decoration: none;
  }
}
</style>
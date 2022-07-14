<template>
  <RouterLink to="/" class="logo">VMDb</RouterLink>
</template>

<style lang="scss" scoped>
.logo {
  font-family: 'Oswald', sans-serif;
  font-size: 32px;
  color: $black;
  text-decoration: none;
  transition: 0.3s;
  &:hover {
    color: $primary;
  }
}
</style>

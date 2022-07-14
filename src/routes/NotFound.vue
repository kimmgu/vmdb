<template>
  <div class="not-found">
    <div class="status">404</div>
    <div class="message">Not Found</div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.not-found {
  line-height: 1.2;
  text-align: center;
  font-family: 'Oswald', sans-serif;
  padding: 80px 20px;
  .status {
    font-size: 128px;
    color: $primary;
  }
  .message {
    font-size: 64px;
  }
}
</style>

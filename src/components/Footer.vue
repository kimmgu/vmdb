<template>
  <footer>
    <!-- <Logo /> -->
    <a href="https://github.com/kmgu/vmdb" target="_blank"
      >© {{ new Date().getFullYear() }} by VMDb, Inc.</a
    >
  </footer>
</template>

<script>
// import Logo from '~/components/Logo.vue'

export default {
  components: {
    // Logo,
  },
}
</script>

<style lang="scss" scoped>
footer {
  padding: 70px 0;
  text-align: center;
  opacity: 0.5;
  a {
    text-decoration: none;
  }
  // .logo {
  //   display: flexbox;
  //   width: 100px;
  //   margin-bottom: 4px;
  // }
}
</style>

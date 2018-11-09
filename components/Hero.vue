<template>
  <section class="hero bg-black" />
</template>

<script>
export default {
  name: 'Hero'
}
</script>

<style lang="scss" scoped>
.hero {
  background: url('~assets/img/hero.jpg');
  background-size: cover;
  background-position-x: 100%;
  filter: grayscale(100%);
  min-height: calc(100vh - 0px);
}
</style>

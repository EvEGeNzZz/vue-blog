<template>
  <div class="container" :class="{ ['container_size_' + size]: size }">
    <slot />
  </div>
</template>

<script>
  export default {
    props: ["size"]
  }
</script>

<style>
  .container {
    position: relative;
    display: block;
    clear: both;
    margin: 0 auto;
    max-width: 980px;
    min-width: 320px;
    min-height: 500px;
  }
  .container_size_l {
    padding: 0 10px;
    max-width: 1200px;
    margin: 50px auto 0;
  }
</style>
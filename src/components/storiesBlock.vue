<template>
  <div class="stories-block" :class="{ ['stories-block__' + rowSize]: rowSize }">
    <slot />
  </div>
</template>

<script>
export default {
  props: {
    rowSize: String
  }
}
</script>

<style>
  .stories-block {
    width: 100%;
    display: flex;
    flex-wrap: wrap;
    align-items: flex-start;
    align-content: flex-start;
    justify-content: space-evenly;
    margin-bottom: 40px;
    padding: 0 20px;
    box-sizing: border-box;
  }
</style>
<template>
    <div class="chip cursor-pointer d-flex align-center">
      <slot />
    </div>
</template>

<script>
  export default {
    name: 'MenuChip'
  }
</script>

<style scoped>
  .chip {
    padding: 8px 16px;
    box-shadow: 0 8px 16px rgba(0 0 0 / 10%);
    border-radius: 20px;
    font-size: 12px;
    color: #434343;
    position: relative;
    top: 0;
    margin-right: 12px;

    transition: .3s;
  }
  .chip:hover {
    top: -4px
  }
</style>
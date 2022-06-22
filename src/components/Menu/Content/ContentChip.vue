<template>
  <div 
    :class="[
      'chip font-weight-medium cursor-pointer', 
      {'active' : chip.isActive }
    ]"
  >
    {{ chip.text }}
  </div>
</template>

<script>
  export default {
    name: 'ContentChip',
    props: {
      chip: {
        type: Object,
        required: true
      }
    } 
  }
</script>

<style scoped>
  .chip {
    padding: 8px 16px;
    color: #212121;
    border-radius: 20px;
    font-size: 14px;
  }
  .chip:hover {
    background: #ebebeb;
  }
  .active {
    background: #E3E4E6;
  }
</style>
<template>
    <div>
        <div class="restaurant__wrapper">
            <div class="content-chips d-flex align-center">
            <content-chip 
              v-for="chip in content.chipCategory" 
              :key="chip.id" 
              :chip="chip" 
            />  
            </div>
            <content-food :foods="content.foods" />
        </div>
    </div>
</template>

<script>
  import ContentChip from './ContentChip.vue'
  import ContentFood from './ContentFood.vue'

  export default {
    name: 'MenuContent',
    components: {
      ContentChip,
      ContentFood
    },
    props: {
      content: {
        type: Object,
        required: true
      }
    }
  }
</script>

<style scoped>
  .restaurant__wrapper {
    width: 85%;
  }
</style>
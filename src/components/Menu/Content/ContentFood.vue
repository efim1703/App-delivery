<template>
  <div class="mt-6">
    <food-item 
      v-for="food in foods" 
      :key="food.id" 
      :food-item="food" 
    />
  </div>
</template>

<script>
  import FoodItem from './FoodItem.vue'

  export default {
    name: 'ContentFood',
    components: {
      FoodItem
    },
    props: {
      foods: {
        type: Array,
        required: true
      }
    }
  }
</script>

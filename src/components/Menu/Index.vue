<template>
  <div class="restaurant">
    <div class="restaurant-title">
      <p>Все рестораны</p>
      <h1>{{ restaurant.title }}</h1>
      <div class="d-flex align-center">
          <menu-chip 
            v-for="chip in restaurant.info" 
            :key="chip.id"
          >
            <mdicon 
              v-if="chip.icon" 
              :name="chip.icon" 
              size="14"
              class="mr-1"
            /> 
            <span>{{ chip.text }}</span>
          </menu-chip>
      </div>
    </div>
    <menu-content 
      class="restaurant-content" 
      :content="restaurant.content"  
    />
  </div>
</template>

<script>
  import MenuChip from './MenuChip.vue'
  import MenuContent from './Content/Index.vue'

  export default {
    name: "TheMenu",
    components: {
      MenuChip,
      MenuContent
    },
    props: {
      restaurant: {
        type: Object,
        required: true
      }
    }
  }
</script>

<style scoped>
  .restaurant-title {
    padding: 88px 0 22px 72px;
    color: #212121;
  }
  h1 {
    margin-top: 26px;
    margin-bottom: 12px;
    font-size: 46px;
  }
  .restaurant-content {
    background: #F6F6F6;
    padding-left: 72px;
    padding: 56px;
  }
</style>
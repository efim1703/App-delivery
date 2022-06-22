<template>
    <div>
      <p>{{ foodItem.title }}</p>
      <div class="food-list d-flex align-center mt-6 mb-8">
        <article 
          class="food-item" 
          v-for="food in foodItem.items" 
          :key="food.id"
        >
          <img 
            class="mt-4" 
            :src="require(`@/assets/${food.img}`)"
          />
          <div class="food-info-content font-weight-medium pa-5">
            <p>{{ food.title }}</p>
            <small class="d-flex mt-1 text-grey">
              {{ food.text }}
            </small>
            <div class="price-box d-flex justify-content-between">
              <p class="font-weight-medium mt-9">
                {{ food.price }}
                <mdicon name="currency-rub" size="16" />
              </p>
              <button class="mt-8 cursor-pointer">
                В корзину
              </button>
            </div>
            <div class="hover-info font-weight-normal">
                <p class="font-weight-medium">{{ food.title }}</p>
                <small class="d-flex mt-1 text-grey">
                  {{ food.text }}
                </small>
                <p class="food-description mt-4">
                  Lorem ipsum dolor sit amet consectetur adipisicing elit. Itaque delectus enim eaque ab. Iusto ipsum aut similique, ex sint error. Animi veritatis repellendus ut nobis libero corrupti quisquam? Nostrum, deleniti.
                </p>
            </div>
          </div>
        </article>
      </div>
    </div>
</template>

<script>
  export default {
    name: "FoodItem",
    props: {
      foodItem: {
        type: Object,
        required: true
      }
    }
  }
</script>

<style scoped>
  .food-list {
    gap: 30px;
    flex-wrap: wrap;
  }
  .food-item {
    width: calc(100% / 5 - 30px);
    background: #FFF;
    box-shadow: 0 8px 16px rgba(0 0 0 / 10%);
    border-radius: 20px;
  }
  .food-item img {
    width: 100%;
    height: auto;
    object-fit: cover;
  }
  .food-info-content {
    position: relative;
  }
  .food-description {
    font-size: 14px;
    color: #434343;
  }
  .hover-info {
    bottom: 70px;
    padding-top: 16px;
    position: absolute;
    background: #fff;
    opacity: 0;
    left: 0;
    width: 100%;
    padding: 16px;
    transition: .3s;
  }
  .price-box button {
    background: #0ec645;
    border: none;
    color: #fff;
    padding: 8px 16px;
    border-radius: 20px;
    opacity: 0;
    transition: .3s;
  }

  article:hover .hover-info,
  article:hover .price-box button {
    opacity: 1;
  }
</style>
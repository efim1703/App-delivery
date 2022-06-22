<template>
  <div id="app">
    <the-header class="header-fixed" />
    <the-menu :restaurant="restaurant" />
    <basket-panel class="basket-fixed" />
  </div>
</template>

<script>
import TheHeader from '@/components/Header/Index.vue'
import TheMenu from '@/components/Menu/Index.vue'
import BasketPanel from './components/BasketPanel.vue'

export default {
  name: 'App',
  components: {
    TheHeader,
    TheMenu,
    BasketPanel
  },
  data() {
    return {
      restaurant: {
        title: 'KFC',
        info: [
          { id: 1, text: '35-35 мин', icon: 'clock-time-two-outline' },
          { id: 2, text: 'От 1 Р' },
          { id: 3, text: 'Доставка 0-269 Р' },
          { id: 4, text: '4,5 - 22653 отзыва', icon: 'star' }
        ],
        content: {
          chipCategory: [
            { id: 1, isActive: true, text: 'Популярные' },
            { id: 2, isActive: false, text: 'Новинки' },
            { id: 3, isActive: false, text: 'Бургеры' },
            { id: 4, isActive: false, text: 'Комбо' },
            { id: 5, isActive: false, text: 'Твистеры' },
          ],
          foods: [
            {
              id: 1,
              title: 'Популярное',
              items: [
                {
                  id: 1,
                  img: 'chiken.webp',
                  title: 'Баскет L 26 крыльев',
                  text: '300 ккал',
                  price: '734'
                },
                {
                  id: 2,
                  img: 'free.webp',
                  title: 'Картошка фри средняя',
                  text: '135 ккал',
                  price: '179'
                },
                {
                  id: 3,
                  img: 'roll.webp',
                  title: 'Твистер острый',
                  text: '80 ккал',
                  price: '225'
                },
                {
                  id: 4,
                  img: 'chiken.webp',
                  title: 'Баскет L 26 крыльев',
                  text: '300 ккал',
                  price: '734'
                },
                {
                  id: 5,
                  img: 'free.webp',
                  title: 'Картошка фри средняя',
                  text: '135 ккал',
                  price: '179'
                },
                {
                  id: 6,
                  img: 'roll.webp',
                  title: 'Твистер острый',
                  text: '80 ккал',
                  price: '225'
                },
                {
                  id: 7,
                  img: 'chiken.webp',
                  title: 'Баскет L 26 крыльев',
                  text: '300 ккал',
                  price: '734'
                },
                {
                  id: 8,
                  img: 'free.webp',
                  title: 'Картошка фри средняя',
                  text: '135 ккал',
                  price: '179'
                },
                {
                  id: 9,
                  img: 'roll.webp',
                  title: 'Твистер острый',
                  text: '80 ккал',
                  price: '225'
                }
              ]
            },
            {
              id: 2,
              title: 'Новинки',
              items: [
                {
                  id: 1,
                  img: 'chiken.webp',
                  title: 'Баскет L 26 крыльев',
                  text: '300 ккал',
                  price: '734'
                },
                {
                  id: 2,
                  img: 'free.webp',
                  title: 'Картошка фри средняя',
                  text: '135 ккал',
                  price: '179'
                },
                {
                  id: 3,
                  img: 'roll.webp',
                  title: 'Твистер острый',
                  text: '80 ккал',
                  price: '225'
                }
              ]
            }
          ]
        }
      }
    }
  }
}
</script>

<style>
@import url('@/assets/css/base.css');
@import url('@/assets/css/lib.css');
.header-fixed {
  position: fixed;
  width: 100%;
  background: #fff;
  z-index: 1;
}
.basket-fixed {
  position: fixed;
  width: 283px;
  height: calc(100vh - 73px);
  top: 73px;
  right: 0;
  background: #fff;
  box-shadow: 0 8px 16px rgba( 64 64 64 / 10% );
}
</style>
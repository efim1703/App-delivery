<template>
  <div>
    <div class="header d-flex align-center full-width">
      <div class="header__logo font-weight-medium cursor-pointer">
        Delivery <br> Club
      </div>

      <header-search class="header__search d-flex align-center" />

      <div class="header__signin d-flex align-center justify-content-end font-weight-medium cursor-pointer">
        <mdicon name="account" class="mr-1" size="18" />
        Войти
      </div>
      <div class="header__buskit d-flex align-center justify-content-end font-weight-medium">
        <mdicon name="basket" class="mr-1" size="18" />
        Корзина
      </div>
    </div>
  </div>
</template>

<script>
  import HeaderSearch from './HeaderSearch.vue'

  export default {
    name: "TheHeader",
    components: {
      HeaderSearch
    }
  }
</script>

<style scoped>
  .header > div {
    border-bottom: 1px solid #e3e4e6;
    border-right: 1px solid #e3e4e6;
    padding: 16px 32px;
    min-height: 72px;
  }
  .header__search {
    flex: 1 1 auto !important;
    border: none !important;
    padding: 0 !important;
    min-height: auto !important;
  }
  .header__buskit {
    border-bottom: 1px solid transparent !important;
  }
</style>

<template>
    <div class="header__search">
        <div v-show="searchIsShown" class="address d-flex align-center full-width">
            <div class="search-address">Москва, улица Введенского, 26</div>
            <button 
                class="search-btn font-weight-medium cursor-pointer"
                @click="searchIsShown = !searchIsShown"
            >
                <mdicon name="clipboard-text-search" class="mr-1" size="18" />
                Поиск
            </button>
        </div>
        <div v-show="!searchIsShown" class="search d-flex align-center full-width"> 
            <div class="search__wrapper full-width d-flex align-center">
                <input 
                    type="text" 
                    class="full-width" 
                    placeholder="Ресторан, блюдо или товар"
                >
                <button 
                    class="cursor-pointer"
                    @click="searchIsShown = !searchIsShown"
                >
                   <mdicon name="close" />
                </button>
            </div>
        </div>
    </div>
</template>

<script>
  export default {
    name: 'HeaderSearch',
    data() {
      return {
        searchIsShown: true
      }
    }
  }
</script>

<style scoped>
    div.header__search {
        width: 100%;
        min-height: 72px !important;
        border-bottom: 1px solid #e3e4e6 !important;
    }
    .search-address {
        flex: 1 1 auto;
        padding: 16px 32px;
    }
    .search-btn {
        border-left: 1px solid #e3e4e6 !important;
        border-right: 1px solid #e3e4e6 !important;
        min-height: 72px;
        padding: 16px 32px;
        background: transparent;
        border: none;
        font-size: 16px;
        font-weight: 600;
    }
    .search {
        min-height: 72px;
        max-height: 72px;
        padding: 16px 32px;
        border-right: 1px solid #e3e4e6 !important;
    }
    .search__wrapper {
        padding: 8px 16px;
        box-shadow: 0 8px 16px rgba(0 0 0 / 10%);
        border-radius: 30px;
    }
    .search__wrapper input {
        padding: 0 8px;
        border: none;
        outline: none;
        font-size: 16px;
    }
    .search__wrapper > button {
        font-size: 24px;
        color: #9C9C9C;
        padding: 0 8px;
        border: none;
        background: transparent;
    }
</style>

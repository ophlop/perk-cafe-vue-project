<template>
    <header>
        <img src="../assets/logo-white.png" alt="logo perk cafe" class="img_logo">
        <AppMenuList :menu="menuUrl" :wrap="wrapClass" :width="widthClass" :color="colorClassDark"/>
        <app-button :activeUrl="reserveUrl" :btnColor="btnColor">Забронировать</app-button>
    </header>
</template>

<script>
import AppMenuList from './UI/AppMenuList.vue'
import AppButton from './UI/AppButton.vue'

export default {
  data () {
    return {
      menuUrl: [
        { title: 'Меню', url: 'https://perkcafe.ru/web-menu' },
        { title: 'Доставка', url: 'https://perkcafe.ru/delivery_perk' },
        { title: 'Gastro Club', url: 'https://perkcafe.ru/bonus' },
        { title: 'Контакты', url: 'https://perkcafe.ru/web-menu' }
      ],
      reserveUrl: 'https://perkcafe.ru/#rec362132297',
      wrapClass: 'nowrap',
      widthClass: 'width-50',
      colorClassDark: 'colorLight',
      btnColor: 'btn-light'
    }
  },
  components: { AppMenuList, AppButton }
}
</script>

<style>
    header {
        width: 1300px;
        height: 100px;
        position: absolute;
        display: flex;
        top: 20px;
        left: 50%;
        transform: translate(-50%);
        padding: 10px;
        justify-content: space-between;
        align-items: center;
    }

    .img_logo {
        width: auto;
        height: 90px;
    }
</style>

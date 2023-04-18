<template>
  <footer>
    <div class="info">
        <h2>Контакты</h2>
        <div class="contacts-info">
            <div class="contacts-mode">
                <h3>Режим работы</h3>
                <h3>ПН - ПТ 8:00 - 23:00</h3>
                <h3>СБ - ВС 9:00 - 23:00</h3>
                <p style="margin-top: 20px;">Завтраки ежедневно до 12:00</p>
                <p>Адрес: ул. Вольская, 63/69, Саратов</p>
                <p>Телефон: 8 (845) 267-75-19</p>
            </div>
            <div class="contacts-info-plus">
                <div class="contacts-info-menu_list">
                    <AppMenuList :menu="menuUrl" :wrap="wrapClass" :width="widthClass" :color="colorClassDark"/>
                </div>
                <div class="contacts-info-btn">
                    <app-button :btnColor="btnColor">Как добраться?</app-button>
                    <app-button :btnColor="btnColor">Оставить Отзыв</app-button>
                </div>
            </div>
        </div>
    </div>
    <div class="map">
        <iframe
            src="https://yandex.ru/map-widget/v1/?um=constructor%3Ab7bed69b9c6bfdc7e728b2bdcdda4d8264e0db782bd10f246bc034f4e2ee7f9a&amp;source=constructor"
            width="400"
            height="400"
            frameborder="0"
            allowfullscreen="true">
        </iframe>
    </div>
  </footer>
</template>

<script>
import AppButton from './UI/AppButton.vue'
import AppMenuList from './UI/AppMenuList.vue'

export default {
  data () {
    return {
      menuUrl: [
        { title: 'PERK', url: 'https://perkcafe.ru/web-menu' },
        { title: 'Доставка', url: 'https://perkcafe.ru/delivery_perk' },
        { title: 'Бронирование', url: 'https://perkcafe.ru/delivery_perk' },
        { title: 'Gastro Club', url: 'https://perkcafe.ru/bonus' },
        { title: 'Вакансии', url: 'https://perkcafe.ru/bonus' },
        { title: 'Поставщикам', url: 'https://perkcafe.ru/web-menu' }
      ],
      wrapClass: 'wrap',
      widthClass: 'width-100',
      colorClassDark: 'colorDark',
      btnColor: 'btn-dark'
    }
  },
  components: { AppButton, AppMenuList }
}
</script>

<style>
footer {
    width: 100vw;
    background-color: #baaca1;
    padding-top: 30px;
}

.info {
    width: 1300px;
    position: relative;
    display: block;
    height: 360px;
    margin: 0 auto 0;
}

.info > h2 {
    margin-top: 0;
    font-size: 30px;
    font-weight: 400;
    text-transform: uppercase;
    letter-spacing: 0.3px;
    color: #3d4549;
}

.contacts-info{
    width: 1300px;
    height: 500px;
    display: inline-flex;
    height: fit-content;
}

.contacts-mode {
    width: 50%;
}

.contacts-mode > h3 {
    margin-top: 0;
    margin-bottom: 0;
    font-size: 20px;
    font-weight: 600;
    text-transform: uppercase;
    letter-spacing: 0.3px;
    color: #3d4549;
}

.contacts-mode > p {
    margin-top: 0px;
    margin-bottom: 6px;
    font-size: 18px;
    font-weight: 400;
    color: #3d4549;
}

.contacts-info-btn{
    margin-top: 50px;
    display: inline-flex;
    gap: 40px;
}

iframe {
    width: 100vw;
}
</style>

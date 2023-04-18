<template>
  <div class="bg">
    <div class="bottom_info">
        <div class="info">
            <span class="text">
                {{ textAbout }}
            </span>
            <div style="margin-bottom: 30px; width: 100%,"></div>
            <div style="width: fit-content; margin: 0 auto;">
                <app-button :btnColor="btnColor">Забронировать</app-button>
            </div>
        </div>
    </div>
  </div>
</template>

<script>
import AppButton from './UI/AppButton.vue'

export default {
  data () {
    return {
      textAbout: `Гастробистро с современным интерьером и внимательным сервисом. Авторские версии любимых блюд в центре гастрономического кластера нашего города.
                В меню представлены блюда, вдохновленные гастро-поинтами разных стран (от Азии до Европы).
                PERK выпекает домашний хлеб, который подается гостям в качестве комплимента, а также самые сливочные круассаны в городе.
                Ежедневно, до 12:00 дня, ждем вас на завтраки в PERK gastrobistro,
                а после 12:00 действует основное меню.`,
      btnColor: 'btn-light'
    }
  },
  components: { AppButton }
}
</script>

<style>
.bg {
    width: 100vw;
    height: 100vh;
    background-position: center;
    background-size: cover;
    background-repeat: no-repeat;
    overflow: hidden;
    overflow-x: none;
    overflow-y: none;
    background-image: url('../assets/bgFirstDisplay.jpg');
}

.bottom_info {
    width: 1300px;
    height: auto;
    position: relative;
    margin: 0 auto;
    bottom: -76vh;
}

.info {
    width: 100%;
    height: fit-content;
    display: block;
    justify-content: center;
    align-items: center;
}

.text {
    width: 100%;
    height: auto;
    color: #ffffff;
    font-size: 16px;
    line-height: 0.4rem;
    margin-bottom: 20px;
}
</style>

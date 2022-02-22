<template>
  <div class="rate-page">
    <h2 class="rate__title">Выберите подходящий Вам тариф qoob.store</h2>
    <div class="rate__info info">
      <p class="info__date">Лицензия Вашего аккаунта окончена 24.12.2021</p>
      <p class="info__rate">Тариф: <b>“Стандарт”</b></p>
      <p class="info__days">6 дней назад</p>
    </div>
    <p class="rate__recommendation">Рекомендуем вам опробовать тариф <b>“Базовый”</b></p>

    <ul class="card-list">
      <li v-for="(item, index) in cardList" :key="index">
        <card-component
          :parentData="item"
        />
      </li>
    </ul>

  </div>
</template>

<script>
import cardComponent from './components/card-component';
import { cardList } from './data.json';

export default {
  name: 'App',
  components: {
    cardComponent: cardComponent
  },
  setup() {
    return { cardList };
  }
}
</script>

<style src="./assets/fonts/style.css"></style>
<style src="./assets/css/style.css"></style>

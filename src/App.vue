<script setup>
import calendar from './components/calendar.vue';
</script>

<template>
  <div class="container">

    <div class="hero hero-tint section light-green">
      <h1>Анна & Юрий</h1>

      <div class="hero-img"></div>

      <h1>17.07.2024</h1>
    </div>

    <div class="section light-brown mix">
      <h2>Дорогие родные
        и друзья!</h2>
      <p style="opacity: 0.6;">В этот день мы хотим собраться в окружении самых любимых и
        дорогих для нас людей.
        С большой радостью приглашаем Вас отпраздновать день нашей
        свадьбы.</p>
      <h2>~ ∞ ~</h2>
    </div>

    <div class="section light-green">
      <h2>День бракосочетания</h2>
      <calendar />
      <h2>~ ∞ ~</h2>
    </div>

  </div>
</template>

<style lang="scss">
@import "./style.scss";

.container {
  width: 380px;
  margin: 0 auto;

  @media (max-width: 380px) {
    width: calc(380px - 40px);
    margin: 0 20px;
  }

}

.section {
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
}

.hero {
  &-img {
    width: 250px;
    height: 250px;
    background: url("./img/hero.jpg") no-repeat top -40px center;
    overflow: hidden;
    background-size: 150%;
    background-position: top 100px;
    border-radius: 125px;
    border: 2px dashed $brown;
  }

}

.hero-tint {
  background-color: rgba(0, 0, 0, 0.2);
  background-blend-mode: multiply;
}

.light-green {
  background-color: color-mix(in srgb, $green 8%, transparent);
}

.light-brown {
  background-color: color-mix(in srgb, $brown 18%, transparent);
}

.img-card {
  width: 270px;
  padding: 5px;
  background-color: white;
  -webkit-box-shadow: 0px 23px 25px -8px rgba(34, 60, 80, 0.36);
  -moz-box-shadow: 0px 23px 25px -8px rgba(34, 60, 80, 0.36);
  box-shadow: 0px 23px 25px -8px rgba(34, 60, 80, 0.36);
}

.yuri {
  position: absolute;
  width: 60%;
  text-align: center;
  bottom: -40px;
  padding: 15px;
  background-color: white;
  border-radius: 0 50px 0 50px;
  font-size: 2rem;
  color: $brown;
}

.anna {
  position: absolute;
  width: 60%;
  text-align: center;
  top: -50px;
  right: 0;
  padding: 15px;
  background-color: white;
  border-radius: 0 50px 0 50px;
  font-size: rem;
  color: $brown;
}

.date {
  position: absolute;
  width: 60%;
  padding: 15px;
  top: 50%;
  left: 50%;

  transform: translate(-50%, -50%);
  font-size: 3rem;
  opacity: 1;
  font-family: "Headers", sans-serif;
  text-shadow: 3px 3px #1b1d32, #000 1px 0 10px;
  color: white;
}

.mix {
  background: color-mix(in srgb, $green 8%, transparent);
  background: linear-gradient(90deg, color-mix(in srgb, $green 28%, transparent) 0%, color-mix(in srgb, $brown 28%, transparent) 100%);
}
</style>


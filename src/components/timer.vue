<template>
    <div class="root mt-4">
        <span class="part">
            <div class="num">{{ days }}</div>
            <div class="title">~ Дней ~</div>
        </span>
        <span class="part">
            <div class="num">{{ hours }}</div>
            <div class="title">~ Часов ~</div>
        </span>
        <span class="part">
            <div class="num">{{ minutes }}</div>
            <div class="title">~ Минут ~</div>
        </span>
        <span class="part">
            <div class="num">{{ seconds }}</div>
            <div class="title">~ Секунд ~</div>
        </span>
    </div>
</template>

<script setup>
import { ref, onMounted } from "vue";

const eventDate = new Date("2024-07-17T12:15:00");
const days = ref(0);
const hours = ref(0);
const minutes = ref(0);
const seconds = ref(0);

const timeRemaining = () => {
    let now = new Date().getTime();
    let distance = eventDate - now;

    days.value = Math.floor(distance / (1000 * 60 * 60 * 24));
    hours.value = Math.floor(
        (distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60)
    );
    minutes.value = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
    seconds.value = Math.floor((distance % (1000 * 60)) / 1000);
};

onMounted(() => {
    setInterval(timeRemaining, 1000);
});
</script>

<style lang="scss" scoped>
@import "../style.scss";
.root {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    grid-template-rows: 1fr;
    grid-column-gap: 2rem;
    grid-row-gap: 0px;
}
.part {
    display: flex;
    align-items: center;
    flex-direction: column;
    & .num {
        font-family: "Headers", sans-serif;
        font-size: 4rem;
        text-shadow: 3px 3px #ffffff,
    }

    & .title {
        font-family: "Text", sans-serif;
        opacity: 0.6;
        font-size: 1rem;
    }
}
</style>

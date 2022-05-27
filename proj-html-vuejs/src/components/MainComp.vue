<template>
<main>
    <MainServices />
    <MainJumbo />
    <section class="slider"></section>
    <section class="pricing"></section>
    <section class="latest"></section>
    <section class="reviews"></section>
</main>
</template>

<script>
import MainJumbo from './main_comps/MainJumbo.vue';
import MainServices from './main_comps/MainServices.vue';
export default {
    components: { MainJumbo, MainServices }
}
</script>

<style scoped lang="scss">

</style>
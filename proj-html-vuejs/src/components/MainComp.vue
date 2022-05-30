<template>
<main>
    <MainServices />
    <MainJumbo />
    <section class="slider"></section>
    <MainPricing />
    <section class="latest"></section>
    <section class="reviews"></section>
</main>
</template>

<script>
import MainJumbo from './main_comps/MainJumbo.vue';
import MainServices from './main_comps/MainServices.vue';
import MainPricing from './main_comps/MainPricing.vue';
export default {
    components: { MainJumbo, MainServices, MainPricing }
}
</script>

<style scoped lang="scss">

</style>
<template>
<main>
    <MainServices />
    <MainJumbo />
    <section class="slider"></section>
    <MainPricing />
    <MainLatest />
    <section class="reviews"></section>
</main>
</template>

<script>
import MainJumbo from './main_comps/MainJumbo.vue';
import MainServices from './main_comps/MainServices.vue';
import MainPricing from './main_comps/MainPricing.vue';
import MainLatest from './main_comps/MainLatest.vue';
export default {
    components: { MainJumbo, MainServices, MainPricing, MainLatest }
}
</script>

<style scoped lang="scss">

</style>
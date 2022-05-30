<template>
<main>
    <MainServices />
    <MainJumbo />
    <section class="slider"></section>
    <MainPricing />
    <MainLatest />
    <MainReviews />
</main>
</template>

<script>
import MainJumbo from './main_comps/MainJumbo.vue';
import MainServices from './main_comps/MainServices.vue';
import MainPricing from './main_comps/MainPricing.vue';
import MainLatest from './main_comps/MainLatest.vue';
import MainReviews from './main_comps/MainReviews.vue';
export default {
    components: { MainJumbo, MainServices, MainPricing, MainLatest, MainReviews }
}
</script>

<style scoped lang="scss">

</style>
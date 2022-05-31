<template>
<main>
    <MainServices />
    <MainJumbo />
    <MainSlider />
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
import MainSlider from './main_comps/MainSlider.vue';
export default {
    components: { MainJumbo, MainServices, MainPricing, MainLatest, MainReviews, MainSlider }
}
</script>

<style scoped lang="scss">

</style>
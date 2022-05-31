<template>
<section>
    <div class="container d-flex justify-content-between">
        <TripleTitle
            class="text-start"
            :redText="this.tripleTitleOne"
            :strongText="this.tripleTitleTwo"
            :regularText="this.tripleTitleThree"
        />
        <div class="icon-container">
            <!-- <div @click="goBack()" class="previus">
                <i class="fas fa-arrow-left"></i>
            </div>
            <div class="next">
                <i class="fas fa-arrow-right"></i>
            </div> -->
        </div>
    </div>
    <div class="carousel">
        <Carousel :items-to-show="3.5" :wrap-around="true">
        <Slide v-for="slide in 8" :key="slide">
            <div class="carousel__item d-flex justify-content-center align-items-center">
                <div
                    class="card"
                    v-for="(el, i) in cardsArray"
                    v-show="(i+1) === slide"
                    :key="i"
                >
                    <div class="img-container">
                        <img :src="el.img" :alt="el.text_one">
                    </div>
                    <div class="txt-container d-flex justify-content-between">
                        <span><strong>{{el.text_one}}</strong></span>
                        <span>{{el.text_two}}</span>
                    </div>
                </div>
            </div>
        </Slide>

        <template #addons>
            <Pagination />
            <Navigation />
        </template>
        </Carousel>
    </div>
    
</section>
</template>

<script>
import { defineComponent } from 'vue';
import { Carousel, Slide, Pagination, Navigation } from 'vue3-carousel';

import 'vue3-carousel/dist/carousel.css';
    
import TripleTitle from '../utils_comp/TripleTitle.vue';

export default defineComponent({
    name: 'WrapAround',
    components: { TripleTitle, Carousel, Slide, Pagination, Navigation},
    data(){
        return{
            // Props per TripleTitle
            tripleTitleOne: "portfolio",
            tripleTitleTwo:"latest",
            tripleTitleThree: "work",
            // Dati cards
            cardsArray:[
                {
                    img: require("../../assets/images/a247b00b-3621-470f-b4b8-b3ac46f25907-1-790x576.jpg"),
                    text_one: "Mock-up Something",
                    text_two: "Digital Experience",
                },
                {
                    img: require("../../assets/images/8wa60okr-1-790x576.jpg"),
                    text_one: "Basket of Flower on table",
                    text_two: "Branding Strategy",
                },
                {
                    img: require("../../assets/images/DRY-1-790x576.jpg"),
                    text_one: "Purinky Products",
                    text_two: "Digital Experience",
                },
                {
                    img: require("../../assets/images/84316050-0af0-49db-a53a-241d47ddad0e-2-790x576.jpg"),
                    text_one: "Satisfy Poster",
                    text_two: "Branding Strategy",
                },
                {
                    img: require("../../assets/images/a247b00b-3621-470f-b4b8-b3ac46f25907-1-790x576.jpg"),
                    text_one: "Mock-up Something",
                    text_two: "Digital Experience",
                },
                {
                    img: require("../../assets/images/8wa60okr-1-790x576.jpg"),
                    text_one: "Basket of Flower on table",
                    text_two: "Branding Strategy",
                },
                {
                    img: require("../../assets/images/DRY-1-790x576.jpg"),
                    text_one: "Purinky Products",
                    text_two: "Digital Experience",
                },
                {
                    img: require("../../assets/images/84316050-0af0-49db-a53a-241d47ddad0e-2-790x576.jpg"),
                    text_one: "Satisfy Poster",
                    text_two: "Branding Strategy",
                },
            ]
        }
    },
    methods:{
        goBack(i){
            i = i-1;
            console.log(i);
        }
    },
    computed:{
        singleCard(){
            let el;
            this.cardsArray.forEach(element => {
                el = element
            });
            return el;
        }
    }

})
</script>

<style scoped lang="scss">
@import '../../assets/style/vars';
section{
    margin: 3rem auto;
    .card{
        width: 80%;
        margin: 3rem 3%;
        border-radius: 20px;
        overflow: hidden;
        box-shadow: 0 0 20px 1px $bg-grey;
        flex-shrink: 0;
        .img-container{
            width: 100%;
            border-radius: 20px;
            overflow: hidden;
            img{
                width: 100%;
            }
        }
        .txt-container{
            padding: 10px;
        }
        &:hover{
            background: linear-gradient(90deg, $magenta, $txt-red);
            color: white;
        }
    }
}
.carousel{
    max-width: 97vw;
    margin: 0 auto;
}

</style>
<template>
<section>
    <div class="first-row">
        <div>
            <TripleTitle 
                :redText="this.tripleTitleOne"
                :strongText="this.tripleTitleTwo"
                :regularText="this.tripleTitleThree"
                :descriptionText="this.tripleTitleFour"
            />
        </div>
    </div>
    <div class="container my-container">
        <div class="second row justify-content-evenly">
            <div
                class="col-3 my-card text-center"
                :class="isOdd(i)"
                v-for="(el, i) in functionalitiesArray"
                :key="`Functionalities${i}`"
            >
                <div class="titles">
                    <h3>{{el.hOne}}</h3>
                    <p>{{el.hTwo}}</p>
                </div>
                <div class="price-shadow">
                    {{el.price}}
                </div>
                <div class="price">
                    <p class="currency">$</p>
                    <p class="number">{{el.price}}</p>
                    <p class="time">Per Month</p>
                </div>
                <div class="functionalities">
                    <p v-for="(obj, num) in el.functions" :key="`Functions${num}`">
                        <span class="bold">{{obj.text_first}}</span>
                        <span class="thin">{{obj.text_second}}</span>
                    </p>
                </div>
                <div class="btn-container">
                    BTN COMP
                </div>
            </div>
        </div>
    </div>

</section>
</template>

<script>
import TripleTitle from '../utils_comp/TripleTitle.vue';
export default {
    components: { TripleTitle },
    data(){
        return{
            // Props per TripleTitle
            tripleTitleOne: "price list",
            tripleTitleTwo:"our",
            tripleTitleThree: "pricing",
            tripleTitleFour: "When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper surface .",
            // Data per card prodotti
            functionalitiesArray:[
                {
                    hOne: "Designing",
                    hTwo: "Process",
                    price: "40",
                    functions:[
                        {
                            text_first: "Creative",
                            text_second: "Design Enabled",
                        },
                        {
                            text_first: "Vibrant",
                            text_second: "Color Usage",
                        },
                        {
                            text_first: "eye",
                            text_second: "Catching Design",
                        },
                        {
                            text_first: "extreme",
                            text_second: "Typography",
                        },
                        {
                            text_first: "exceptional",
                            text_second: "Design",
                        },
                    ]
                },
                {
                    hOne: "Developing",
                    hTwo: "Product",
                    price: "60",
                                        functions:[
                        {
                            text_first: "Creative",
                            text_second: "Design Enabled",
                        },
                        {
                            text_first: "Vibrant",
                            text_second: "Color Usage",
                        },
                        {
                            text_first: "eye",
                            text_second: "Catching Design",
                        },
                        {
                            text_first: "extreme",
                            text_second: "Typography",
                        },
                        {
                            text_first: "exceptional",
                            text_second: "Design",
                        },
                    ]
                },
                {
                    hOne: "Supporting",
                    hTwo: "clients",
                    price: "80",
                    functions:[
                        {
                            text_first: "Creative",
                            text_second: "Design Enabled",
                        },
                        {
                            text_first: "Vibrant",
                            text_second: "Color Usage",
                        },
                        {
                            text_first: "eye",
                            text_second: "Catching Design",
                        },
                        {
                            text_first: "extreme",
                            text_second: "Typography",
                        },
                        {
                            text_first: "exceptional",
                            text_second: "Design",
                        },
                    ]
                }
            ],
        }
    },
    methods:{
        isOdd(index){
            if(index % 2){
                return "odd";
            }
        }
    }
}
</script>

<style scoped lang="scss">
@import '../../assets/style/vars';

section{
    .first-row{
        background: linear-gradient(90deg, $bg-blue, $bg-dark-4);
        padding: 3rem 0 21rem;
        div{
            margin: 0 15%;
            color: white;
        }
    }

    .my-container{
        transform: translate(0, -55%);
    }
}

.my-card{
    background-color: white;
    width: 22vw;
    border-radius: 5%;
    position: relative;

    .titles{
        margin: 1rem 0;
        h3{
            font-weight: bold;
        }
        p{
            font-size: 12px;
            text-transform: uppercase;
        }
    }
    .price-shadow{
        position: absolute;
        bottom: 40%;
        right: 0;
        font-size: 260px;
        opacity: (0.2);

    }
    .price{
        width: 33%;
        margin: 1rem auto;
        p{
            margin: 0;
        }
        .currency{
            text-align: left;
        }
        .number{
            font-size: 60px;
            font-weight: bold;
        }
        .time{
            font-size: 10px;
            font-weight: 600;

        }
    }
    .functionalities{
        text-transform: capitalize;
        font-size: 14px;
        span.bold{
            font-weight: bold;
            margin-right: 3px;
        }
        span.thin{
            color: #191919;
        }
    }
}

.my-card.odd{
    background: linear-gradient(135deg, $magenta, $txt-red);
    color: white;
    span.thin{
        color: #e0e0e0;
    }
}
</style>
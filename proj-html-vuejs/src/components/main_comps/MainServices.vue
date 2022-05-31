<template>
<section class="container justify-content-center">
    <div class="row title justify-content-center">
        <div class="col-6">
            <TripleTitle 
                :redText="this.tripleTitleOne"
                :strongText="this.tripleTitleTwo"
                :regularText="this.tripleTitleThree"
                :descriptionText="this.tripleTitleFour"
            />
        </div>
    </div>

    <div class="row cards justify-content-evenly">
        <div v-for="(el, i) in cardInfoArray" 
            :key="`ServiceCard${i}`"
            class="col-2 text-center d-flex flex-column justify-content-between">
            <div class="img_container">
                <img :src="el.service_img" :alt="el.service_title">
            </div>
            <div>
                <h5><strong>{{el.service_title}}</strong></h5>
                <p>{{el.service_description}}</p>
            </div>
        </div>
    </div>

    <div class="row button justify-content-center">
        <div class="col-2">
            <ButtonsComp
                :deg="this.BtnDeg"
                :color1="this.BtnColor1"
                :color2="this.BtnColor2"
                :text="this.BtnText"
                :textColor="this.BtnTextColor"
            />
        </div>
    </div>
</section>
</template>

<script>
import TripleTitle from '../utils_comp/TripleTitle.vue';
import ButtonsComp from '../utils_comp/ButtonsComp.vue';
export default {
    components: { TripleTitle, ButtonsComp },
    data() {
        return {
            cardInfoArray: [
                {
                    service_img: require("../../assets/images/Group-247.png"),
                    service_title: "Data Analysis",
                    service_description: "When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper",
                },
                {
                    service_img: require(`../../assets/images/Group-567.png`),
                    service_title: "SEO Optimization",
                    service_description: "When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper",
                },
                {
                    service_img: require("../../assets/images/Group-538.png"),
                    service_title: "Security Data",
                    service_description: "When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper",
                },
                {
                    service_img: require("../../assets/images/Group-566.png"),
                    service_title: "Brending Strategy",
                    service_description: "When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper",
                },
            ],
            // Props per TripleTitle
            tripleTitleOne: "our services",
            tripleTitleTwo:"what",
            tripleTitleThree: "we do",
            tripleTitleFour: "When, while the lovely valley teems with vapour around meand the",

            // Props per ButtonsComp
            BtnDeg: "135deg",
            BtnColor1: "rgb(182, 36, 110)", 
            BtnColor2: "rgb(249, 99, 107)",
            BtnText: "view all services",
            BtnTextColor: "white",
        };
    },
}
</script>

<style scoped lang="scss">
section{
    margin: 3rem auto;
}
.cards{
    .img_container{
        height: 40%;
        margin-top: 5rem;
        img{
            width: 100%;
        }
    }
}
.button.row{
    margin: 5rem 0;
    div{
        box-shadow: 0 0 75px 1px rgb(249, 99, 107);
    }
}
</style>
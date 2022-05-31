<template>
<div class="box">
    <div class="titles">
        <p v-if="jumboPreText" class="pretext">{{jumboPreText}}</p>
        <h1 v-if="jumboFirstText" class="bold">{{jumboFirstText}}</h1>
        <h1 v-if="jumboSecondText" class="thin">{{jumboSecondText}}</h1>
        <h1 v-if="jumboThirdText" class="bold">{{jumboThirdText}}</h1>
    </div>
    <p class="description">{{jumboDescription}}</p>
    <div class="btn-container d-flex">
        <span>
            <ButtonsComp
                :deg="this.deg"
                :color1="this.redColor1"
                :color2="this.redColor2"
                :text="this.redText"
                :textColor="this.textColor"
            />
        </span>
        <span>
            <ButtonsComp
                :deg="this.deg"
                :color1="this.blueColor1"
                :color2="this.blueColor2"
                :text="this.blueText"
                :textColor="this.textColor"
            />
        </span>
    </div>
</div>
</template>

<script>
import ButtonsComp from './ButtonsComp.vue';

export default {
    components: { ButtonsComp},
    props: {
        //Per il testo
        jumboPreText: String,
        jumboFirstText: String,
        jumboSecondText: String,
        jumboThirdText: String,
        jumboDescription: String,
    },
    data(){
        return{
            //Props per JumboBtns
            deg: "90deg",
            textColor: "white",

            redColor1: "rgb(182, 36, 110)",
            redColor2: "rgb(249, 99, 107)",
            redText: "try it now",

            blueColor1: "rgb(3, 166, 210)",
            blueColor2: "rgb(31, 63, 131)",
            blueText: "explore more",
        }
    }
}
</script>

<style scoped lang="scss">
@import '../../assets/style/vars';

.box{
    padding: 1vw;
    width: 30vw;
    .titles{
        color: white;
        text-transform: capitalize;
        h1.bold{
            font-weight: bolder;
        }
    }
    .description{
        color: $txt-blue;
        margin: 2rem 0;
    }
    span{
        width: 150px;
        margin-right: 20px;
    }
}
</style>
<template>
<section>
    <div class="container">
        <div class="row">
            <div class="col-6 image">
                <img class="graphic" src="../../assets/images/nemoodar.png" alt="graphic">
                <img class="men" src="../../assets/images/men-data.png" alt="men-data.png">
            </div>
            <div class="col-6 d-flex align-items-center">
                <JumboCard
                    :jumboPreText="this.jumboOne" 
                    :jumboFirstText="this.jumboTwo"
                    :jumboSecondText="this.jumboThree"
                    :jumboDescription="this.jumboFour"
                />
            </div>
        </div>
    </div>
</section>
</template>

<script>
import JumboCard from "../utils_comp/JumboCard.vue";

export default {
    components: { JumboCard },
    data(){
        return{
            jumboOne: "Start Your Project",
            jumboTwo:"Grow Your Business",
            jumboThree: "With our strategy",
            jumboFour: "When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper surface .of the impenetrable foliage of my trees, and but a few stray gleams steal into the inner sanctuary,",
        }
    }

}
</script>

<style scoped lang="scss">
@import '../../assets/style/vars';

section{
    background: linear-gradient($bg-blue, $bg-dark-4 50%);
    padding: 3rem;
    .image{
        padding: 4rem;
        position: relative;
        .graphic{
            width: 25vw;
            position: absolute;
            top: 1%;
            left: 3%;
        }
        .men{
            width: 25vw;
            position: relative;
        }
    } 
}
</style>
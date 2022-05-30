<template>
<header>
    <div class="container">
        <div class="row">
            <div class="col-12 d-flex justify-content-between align-items-center">
                <div class="logo">
                    <img src="../assets/images/white-logo-2.png" alt="PhloxCorpLogo">
                </div>
                <nav class="d-flex">
                    <a v-for="(el, i) in navLinksArray" :key="`NavLinks${i}`" href="#">{{el}}</a>
                    <div class="my-btn">QUI CI METTO UN BTNCOMP</div>
                </nav>
            </div>
        </div>
        <div class="row">
            <div class="col-6 d-flex align-items-center">
                <JumboCard :jumboFirstText="this.jumboOne" :jumboSecondText="this.jumboTwo" :jumboThirdText="this.jumboThree" :jumboDescription="this.jumboFour"/>
            </div>
            <div class="col-6">
                <img src="../assets/images/header.png" alt="header.png">
            </div>
        </div>
    </div>
</header>
</template>

<script>
import JumboCard from "./utils_comp/JumboCard.vue";

export default {
    components: { JumboCard },
    data() {
        return {
            navLinksArray: [
                "Home",
                "About",
                "Service",
                "Blog",
                "Contact",
                "Portfolio",
            ],
            // Props per JumboCard
            jumboOne: "Business Planning",
            jumboTwo:"Digital Technology",
            jumboThree: "Modern Solution !",
            jumboFour: "When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper surface .",
        };
    },
}
</script>

<style scoped lang="scss">
@import '../assets/style/vars';

header{
    background: linear-gradient($bg-blue, $bg-dark-4 50%);
    padding-bottom: 7.5rem;
    .logo{
        padding: 10px;
    }
    a{
        color: white;
        margin: 0 .5rem;
        &:hover,
        &:focus{
            color: $txt-red;
        }
    }
    .my-btn{
        margin: 0 2rem;
    }
    .col-6 img{
        width: 100%;
    }
}

</style>
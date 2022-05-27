<template>
<div class="box">
    <div class="titles">
        <p v-if="jumboPreText" class="pretext">{{jumboPreText}}</p>
        <h1 v-if="jumboFirstText" class="bold">{{jumboFirstText}}</h1>
        <h1 v-if="jumboSecondText" class="thin">{{jumboSecondText}}</h1>
        <h1 v-if="jumboThirdText" class="bold">{{jumboThirdText}}</h1>
    </div>
    <p class="description">{{jumboDescription}}</p>
    <div class="btn-container">
        <span>BTNCOMP</span>
        <span>BTNCOMP</span>
    </div>
</div>
</template>

<script>

export default {
    props:{
        jumboPreText: String,
        jumboFirstText: String,
        jumboSecondText: String,
        jumboThirdText: String,
        jumboDescription: String,
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
}
</style>
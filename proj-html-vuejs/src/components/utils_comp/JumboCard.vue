<template>
<div class="box">
    <div class="titles">
        <h6 class="pretext">{{jumboPreText}}</h6>
        <h1 class="bold">{{jumboFirstText}}</h1>
        <h1 class="thin">{{jumboSecondText}}</h1>
        <h1 class="bold">{{jumboThirdText}}</h1>
    </div>
    <p>{{jumboDescription}}</p>
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
        h1.bold{
            font-weight: bolder;
        }
    }
    p{
        color: $txt-blue;
        margin: 2rem 0;
    }
}
</style>
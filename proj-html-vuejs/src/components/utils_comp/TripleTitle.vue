<template>
<div>
    <p v-if="redText" class="red-title">{{redText}}</p>
    <h1 v-if="strongText || reguralText">
        <strong>{{strongText}}</strong> {{regularText}}
    </h1>
    <p v-if="descriptionText" class="description">{{descriptionText}}</p>
</div>
</template>

<script>
export default {
    props:{
        redText: String,
        strongText: String,
        regularText: String,
        descriptionText: String,
    }
}
</script>

<style scoped lang="scss">
@import '../../assets/style/vars';

div{
    text-align: center;
    .red-title, h1{
        text-transform: capitalize;
    }
    .red-title{
        color: $txt-red;
    }
    h1{
        margin-bottom: 2rem;
    }
    .description{
        color: $txt-grey;
    }
}

</style>
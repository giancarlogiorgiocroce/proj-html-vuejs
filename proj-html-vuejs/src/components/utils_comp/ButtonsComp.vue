<template>
<div class="d-flex justify-content-center align-items-center" :style="addLinearGradient()">
    <a :style="addTextColor()">
        {{text}}
    </a>
</div>
</template>

<script>
export default {
    props:{
        text: String,
        deg: String,
        color1: String,
        color2: String,
        textColor: String,
    },
    data(){
        return{

        }
    },
    methods:{
        addLinearGradient(){
            console.log(this.color1, this.color2);
            return `background: linear-gradient(${this.deg}, ${this.color1}, ${this.color2})`;
        },
        addTextColor(){
            return `color: ${this.textColor}`;
        }
    }

}
</script>

<style scoped lang="scss">
@import '../../assets/style/vars';
div{
    min-width: 75px;
    padding: 5px;
    border-radius: 15px;
    background-color: white;
}
a{
    text-transform: capitalize;
    font-size: 14px;
    &:hover{
        cursor: pointer;
        color: black !important;
    }
}
</style>
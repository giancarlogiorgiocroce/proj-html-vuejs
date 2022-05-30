<template>
<section class="container">
    <div class="row first">
        <div class="title-container">
            <TripleTitle 
                :redText="this.tripleTitleOne"
                :strongText="this.tripleTitleTwo"
                :regularText="this.tripleTitleThree"
                :descriptionText="this.tripleTitleFour"
            />
        </div>
    </div>
    <div class="row second">
        <div class="col comment-card text-center"
            v-for="(el, i) in commentsArray"
            :key="`Comments${i}`"
        >
            <div class="img-container">
                <img :src="el.image" :alt="el.name">
            </div>
            <div class="vote">
                <i 
                    v-for="i in Math.round(el.vote)/2"
                    :key="`FullStars${i}`"
                    class="fa-star fa-solid">
                </i>
                <i 
                    v-for="i in (5 - Math.round(el.vote)/2) - (Math.round(el.vote) % 2)"
                    :key="`EmptyStars${i}`"
                    class="fa-star fa-regular">
                </i>
            </div>
            <div class="txt-container">
                <p class="description">{{el.description}}</p>
                <p class="name"><strong>{{el.name}}</strong></p>
                <p class="role">{{el.role}}</p>
            </div>

        </div>
    </div>
    <div class="row third">
        <div
            class="col d-flex justify-content-center align-items-center"
            v-for="(el, i) in partnersArray"
            :key="`Partners${i}`"
        >
            <img :src="el.image" :alt="el.partner">
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
            tripleTitleOne: "testimonial",
            tripleTitleTwo:"what",
            tripleTitleThree: "people say",
            tripleTitleFour: "When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper surface .",
            commentsArray:[
                {
                    image: require('../../assets/images/szabo-viktor-1266895-unsplash-1024x1024.png'),
                    vote: 6,
                    description: "When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper impenetrable foliage of my trees, and but a thousand.",
                    name: "Michkel Anegl",
                    role: "Marketing Management",
                },
                {
                    image: require('../../assets/images/philipe-cavalcante-539505-unsplash-1024x1024.png'),
                    vote: 6,
                    description: "When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper impenetrable foliage of my trees, and but a thousand.",
                    name: "Michkel Anegl",
                    role: "Marketing Management",
                },
                {
                    image: require('../../assets/images/fabio-spinelli-695744-unsplash-1024x1024.png'),
                    vote: 6,
                    description: "When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper impenetrable foliage of my trees, and but a thousand.",
                    name: "Michkel Anegl",
                    role: "Marketing Management",
                },
            ],
            partnersArray:[
                {
                    partner: "Golden",
                    image: require("../../assets/images/client-1-1.png")
                },
                {
                    partner: "Sweety Cafeteria",
                    image: require("../../assets/images/clienty-2.png")
                },
                {
                    partner: "Fastlane Sportswear",
                    image: require("../../assets/images/clienty-4.png")
                },
                {
                    partner: "Mighty Fornitures",
                    image: require("../../assets/images/client-5.png")
                },
                {
                    partner: "Jack Roller",
                    image: require("../../assets/images/clienty-3.png")
                },
            ]
        }
    },
}
</script>

<style scoped lang="scss">
@import '../../assets/style/vars';
section{
    margin-top: 3rem;
    .title-container{
        margin: 0 auto;
        width: 52%;
    }
    .row.second{
        margin: 3rem auto;
        .comment-card{
            padding: 20px;
        }
        .img-container{
            height: 12vh;
            width: 12vh;
            margin: 1rem auto;
            border-radius: 50%;
            border: 5px solid $magenta;
            img{
                height: 100%;
            }
        }
        i{
            color: $magenta;
        }
        .txt-container{
            font-size: 14px;
            .description,
            .role{
                color: $txt-grey-2;
            }
        }
    }
    .row.third{
        img{
            width: 40%;
        }
    }
}

</style>
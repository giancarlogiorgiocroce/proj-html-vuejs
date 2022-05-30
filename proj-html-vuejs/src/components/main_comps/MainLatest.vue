<template>
<section class="container">
    <div class="row first">
        <div>
            <TripleTitle 
                :redText="this.tripleTitleOne"
                :strongText="this.tripleTitleTwo"
                :regularText="this.tripleTitleThree"
                :descriptionText="this.tripleTitleFour"
            />
        </div>
    </div>
    <div class="row second justify-content-center">
        <div
            class="my-card d-flex justify-content-between"
            :class="i == 0 ? 'w45 active align-items-end' : 'w20 flex-column'"
            v-for="(el, i) in latestPostArray"
            :key="`LatestPost${i}`"
        >
            <img v-if="i == 0" :src="el.image" :alt="el.title">
            <div class="text">
                <p>{{el.date}}{{el.by}}</p>
                <h6>{{el.title}}</h6>
                <p>{{el.description}}</p>
            </div>
            <div>BTNCOMP</div>
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
            tripleTitleOne: "blog",
            tripleTitleTwo:"latest",
            tripleTitleThree: "posts",
            tripleTitleFour: "When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper surface .",
            // Data per latest posts
            latestPostArray:[
                {
                    date: "April 21,2019 ",
                    by: "· by Paul",
                    title: "Amazon gets CCI nod to acquire 49% stake in...",
                    description: "When, while the lovely valley teems with vapour around meand the meridian sun s...",
                    image: require('../../assets/images/headway-537308-unsplash-1380x703.jpg')
                },
                {
                    date: "April 21,2019 ",
                    by: "· by Paul",
                    title: "Clearing Corporations get SEBI nod to invest in overnights funds",
                    description: "When, while the lovely valley teems with vapour around meand the meridian sun s...",
                    image: require('../../assets/images/headway-537308-unsplash-1380x703.jpg')
                },
                {
                    date: "April 21,2019 ",
                    by: "· by Paul",
                    title: "Shabnam Dillon, wife of RSSB chief Gurinder Dillon, passes away in London",
                    description: "When, while the lovely valley teems with vapour around meand the meridian sun s...",
                    image: require('../../assets/images/headway-537308-unsplash-1380x703.jpg')
                },
            ]
        }
    }
}
</script>

<style scoped lang="scss">
@import '../../assets/style/vars';
.container{
    .row.first{
        div{
            margin: 0 auto 2rem;
            width: 70%;
        }
    }
    .row.second{
        .my-card{
            color:white;
            background: linear-gradient(135deg, $bg-dark-4, $bg-blue 100%);
            padding: 3rem 1rem 2rem;
            margin: 1rem;
            border-radius: 25px;
            .text{
                width: 85%;
                margin-bottom: 1rem;
            }
            p{
                font-size: 13px;
                margin: 0;
            }
            h6{
                margin: 1rem 0;
                font-weight: bold;
            }
        }
        .my-card.active{
            position: relative;
            overflow: hidden;
            .text,div{
                filter: brightness(1);
                margin-bottom: 0;
            }
            img{
                position: absolute;
                top: 0;
                left: 0;
                width: 105%;
                height: 105%;
                border-radius: 25px;
                filter: brightness(0.7);
            }
        }
    }
}

</style>
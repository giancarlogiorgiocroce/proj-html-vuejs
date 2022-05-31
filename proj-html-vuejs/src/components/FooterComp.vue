<template>
<footer>
    <div class="container">
        <div class="searchbar row justify-content-between">
            <div class="col-6">
                <h1>we offer awesome services</h1>
                <p>When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper surface .</p>
            </div>
            <div class="col-5 d-flex justify-content-end align-items-center">
                <div class="email-container d-flex">
                <input type="text">
                    <div class="btn-container">
                        <ButtonsComp
                            :deg="this.BtnDeg"
                            :color1="this.BtnColor1"
                            :color2="this.BtnColor2"
                            :text="this.BtnText"
                            :textColor="this.BtnTextColor"
                        />
                    </div>
                </div>
            </div>
        </div>
        <div class="main row">
            <div class="col">
                <img src="../assets/images/white-logo-2.png" alt="PhloxLogo">
                <p>When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper impenetrable</p>
            </div>
            <div class="col">
                <ul>
                    <li class="text-white">Quick Links</li>
                    <li><a href="#">Service</a></li>
                    <li><a href="#">Contact</a></li>
                    <li><a href="#">Blog</a></li>
                </ul>
            </div>
            <div class="col">
                <ul>
                    <li class="text-white">Resources</li>
                    <li>
                        <ul class="text-center">
                            <li><a href="#">Art Design</a></li>
                            <li><a href="#">Computer</a></li>
                            <li><a href="#">IT News</a></li>
                            <li><a href="#">Networking</a></li>
                            <li><a href="#">Web Securety</a></li>
                        </ul>
                    </li>
                </ul>
            </div>
            <div class="col">
                <ul>
                    <li class="text-white">Contact Us</li>
                    <li><strong class="text-white">Address:</strong> P. Sherman, Wallaby Way, Sydney (AU)</li>
                    <li><strong class="text-white">Phone:</strong> +00 123 456 7890</li>
                    <li><strong class="text-white">Email:</strong> qualcosa@qualcosaltro.com</li>
                </ul>
            </div>
        </div>
    </div>
    <div class="bottom">
        <div class="container d-flex flex-row align-items-center">
            <div class="col-6">
                <p>&copy; 2020 Phlox. All Rights Reserved.</p>
            </div>
            <div class="col-6">
                <div class="icons text-end">
                    <a href="#"><i class="fa-brands fa-instagram"></i></a>
                    <a href="#"><i class="fa-brands fa-linkedin-in"></i></a>
                    <a href="#"><i class="fa-brands fa-facebook-f"></i></a>
                    <a href="#"><i class="fa-brands fa-twitter"></i></a>
                </div>
                <div class="external d-flex">
                    <div>
                        <a href="#" class="arrow-container d-flex align-items-center justify-content-center">
                            <i class="fa-solid fa-arrow-up-long"></i>
                        </a>
                    </div>
                    <div>
                        <a href="#" class="chat-container d-flex align-items-center justify-content-center">
                            <i class="fa-regular fa-comment"></i>
                        </a>
                    </div>
                </div>
            </div>
        </div>
    </div>
</footer>
</template>

<script>
import ButtonsComp from './utils_comp/ButtonsComp.vue'

export default {
    data() {
        return {
            // Props per ButtonsComp
            BtnDeg: "90deg",
            BtnColor1: "rgb(3, 168, 212)", 
            BtnColor2: "rgb(32, 63, 131)",
            BtnText: "subscribe",
            BtnTextColor: "white",
        };
    },
    components: { ButtonsComp }
}
</script>

<style scoped lang="scss">
@import '../assets/style/vars';
footer{
    color: white;
    background: linear-gradient(white 15%, $dark-blue 15%, $dark-blue-2);
    margin: 3rem auto 0;

    .searchbar{
        background: linear-gradient(90deg, $magenta, $txt-red);
        margin: 0 auto;
        padding: 2rem 1rem;
        border-radius: 20px;
        position: relative;
        left: auto;
        bottom: 100%;
        h1{
            text-transform: capitalize;
        }
        p{
            font-size: 12px;
        }
        input{
            border: 0;
            width: 80%;
        }
        .email-container{
            border-radius: 20px;
            padding: 7.5px;
            width: 100%;
            background-color: white;
        }
        .btn-container{
            width: 150px;
        }
    }

    .main.row{        
        margin: 2rem auto;
        p{
            font-size: 13px;
            color: $txt-grey-2;
            margin-top: 2rem;
        }
        ul{
            list-style: none;
            color: $txt-grey-2;
            li{
                margin: 15px;
            }
            a{
                color: $txt-grey-2;
            }
        }
    }    
}

.bottom{
        padding: 10px;
        border-top: .5px solid $txt-grey;
        position: relative;
        p{
            font-size: 13px;
            color: $txt-grey-2;
            margin: 0;
        }
        a{
            color: white;
            margin: 0 .5rem;
        }
    }

    .external{
        position: absolute;
        right: 0;
        top: 0;
        .arrow-container{
            height: 1.5vw;
            width: 1.5vw;
            border-radius: 50%;
            background-color: white;
            i{
                color: black;
                font-size: 10px;
            }
        }
        .chat-container{
            background-color: $bg-blue;
            height: 2.5vw;
            width: 2.5vw;
            border-radius: 50%;
            margin-top: 5px;
            .fa-comment{
                transform: rotateY(180deg);
            }
        }
    }
</style>
<script>

    import Carouselcard from './Carouselcard.vue';

    export default {
        components:{
            Carouselcard
        },
        data(){
            return{

                currentCard: 0,

                CardList: [
                    {
                        id: 1,
                        img: "../assets/8wa60okr-1-790x576.jpg",
                        title: "Basket of Flower table",
                        info: "Branding Strategy"
                    },
                    {
                        id: 2,
                        img: "../assets/DRY-1-790x576.jpg",
                        title: "Purinky products",
                        info: "Digital Experience"
                    },
                    {
                        id: 3,
                        img: "../assets/a247b00b-3621-470f-b4b8-b3ac46f25907-1-790x576.jpg",
                        title: "Satisfy Poster",
                        info: "Branding Strategy"
                    },
                    {
                        id: 4,
                        img: "../assets/84316050-0af0-49db-a53a-241d47ddad0e-2-790x576.jpg",
                        title: "Mock-up Template",
                        info: "E-commerce"
                    },
                    {
                        id: 5,
                        img: "../assets/a247b00b-3621-470f-b4b8-b3ac46f25907-1-790x576.jpg",
                        title: "Landing Page",
                        info: "Digital Experiece"
                    },
                    
                ]
            }
        },

        methods:{
            rightScroll(){
                const wrapper = this.$refs.wrapper;
                const card = this.$refs.card[0];
                const cardWidth = card.offsetWidth;
                console.log(wrapper, card, cardWidth);
                wrapper.scrollLeft += cardWidth;
                if (this.currentCard === this.CardList.length - 1){
                    this.currentCard < this.CardList.length;
                } else {
                    this.currentCard++;
                };
                console.log(this.currentCard, this.CardList.length)
            },

            leftScroll(){
                const wrapper = this.$refs.wrapper;
                const card = this.$refs.card[0];
                const cardWidth = card.offsetWidth;
                console.log(wrapper, card, cardWidth);
                wrapper.scrollLeft -= cardWidth;

                if (this.currentCard <= 0){
                    this.currentCard = 0;
                } else {
                    this.currentCard--;
                };

            },

            dotFunction(index){
                const card = this.$refs.card;
                console.log(card[index], index);
                this.currentCard = index;
                card[index].scrollIntoView({behavior: "smooth", block: "nearest", inline: "start"});
            }
        }
    }
</script>

<template>
    <section class="pe-0">

        <!-- title container text  -->

        <div class="top-container d-flex align-items-center justify-content-between">
            <div class="title-container">
                <div class="section-title-cont">
                    <small class="d-inline-block pb-2 fw-medium">Our Service</small>
                    <h2 class="pb-2"><span class="fw-bold">latest</span> work</h2>
                </div>
            </div>

            <!-- carousel button -->


            <div class="button-container d-flex gap-5">
                <button type="button" class="btn btn-outline-danger" @click="leftScroll(index)">
                    <i class="fa-solid fa-arrow-left"></i>
                </button>
                <button type="button" class="btn btn-outline-danger" @click="rightScroll(index)">
                    <i class="fa-solid fa-arrow-right"></i>
                </button>
            </div>
        </div>

        <!-- CAROUSEL SECTION-->

        <div class="carousel-section">

            <div class="carousel-container d-flex gap-4 overflow-hidden p-3" ref="wrapper">
    
                <div class="card-wrapper" v-for="(singleCard, index) in CardList" :key="index" ref="card">
                    <Carouselcard :carouselObj="singleCard"></Carouselcard>
                </div>
            </div>
    
            <div class="dots-container">
                <i class="fa-solid fa-circle" @click="dotFunction(index)" v-for="(singleCard, index) in CardList" :class="{'active': this.currentCard === index}"></i>
            </div>
        </div>

    </section>
</template>

<style lang="scss" scoped>
    @use "../sass/partials/variables";
    @use "../sass/partials/mixins";

    section{
        margin-top: 7rem;

        .top-container{
            margin-bottom: 5rem;

            h2{
                font-size: variables.$text-section-h2;
            }

            small{
                color: variables.$over-color-text;
                font-size: variables.$text-small-size;
            }
        }

        .carousel-section{

            .carousel-container{
                scroll-behavior: smooth;
            };

            .dots-container{
                display: flex;
                justify-content: center;
                align-items: center;
                gap: .7rem;
                padding-top: 5rem;
                margin-bottom: -3rem;
                font-size: .6rem;
                color: lightgrey;

                i{
                    cursor: pointer;

                }
                
            }
        }

        .active{
            color: variables.$over-color-text;
        }

        .button-container{
            padding-right: 200px;

            button{
                font-size: 1.2rem;
                border-radius: 50%;
                padding: 1rem;
                width: 60px;
                aspect-ratio: 1/1;
                transition: all .3s linear;
    
            &:hover{
                @include mixins.red-hover
                }
            }

        }
    }


</style>
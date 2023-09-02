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
                this.currentCard++;
                console.log(wrapper, card, cardWidth);
                wrapper.scrollLeft += cardWidth;
            },
        }
    }
</script>

<template>
    <section>

        <!-- title container text  -->

        <div class="top-container d-flex align-items-center justify-content-between">
            <div class="title-container">
                <div class="section-title-cont">
                    <small class="d-inline-block pb-2 fw-medium">Our Service</small>
                    <h2 class="fs-1 pb-2"><span class="fw-bold">latest</span> We Do</h2>
                </div>
            </div>

            <!-- carousel button -->


            <div class="button-container d-flex gap-5"  >
                <button type="button" class="btn btn-outline-danger" @click="leftScroll()">
                    <i class="fa-solid fa-arrow-left"></i>
                </button>
                <button type="button" class="btn btn-outline-danger" @click="rightScroll()">
                    <i class="fa-solid fa-arrow-right"></i>
                </button>
            </div>
        </div>

        <!-- CAROUSEL -->

        <div class="carousel-containter d-flex gap-4 overflow-hidden" ref="wrapper">

            <div class="card-wrapper" v-for="(singleCard, index) in CardList" :key="index" ref="card">
                <Carouselcard :carouselObj="singleCard"></Carouselcard>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
    @use "../sass/partials/variables";

    section{
        margin-top: 7rem;

        .top-container{
            margin-bottom: 5rem;
        }


        small{
            color: variables.$over-color-text
        }

        button{
            border-radius: 50%;
        }
    }


</style>
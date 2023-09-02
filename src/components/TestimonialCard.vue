<script>
    import SingleTestimonial from './SingleTestimonial.vue';

    export default{
        components:{
            SingleTestimonial,
        },
        data(){
            return{
                testimonialList: [
                    {
                        photo: "../assets/szabo-viktor-1266895-unsplash-1024x1024.png",
                        comment: "When, while lovelyvalley teems with vapour around meand meridian sun strikes the upper impenetrable foliage of my trees, and but a thousand.",
                        name: "Michkel Anegl",
                        role: "Marketing Managment"
                    },
                    {
                        photo: "../assets/philipe-cavalcante-539505-unsplash-1024x1024.png",
                        comment: "When, while lovelyvalley teems with vapour around meand meridian sun strikes the upper impenetrable foliage of my trees, and but a thousand.",
                        name: "Michkel Anegl",
                        role: "Marketing Managment"
                    },
                    {
                        photo: "../assets/fabio-spinelli-695744-unsplash-1024x1024.png",
                        comment: "When, while lovelyvalley teems with vapour around meand meridian sun strikes the upper impenetrable foliage of my trees, and but a thousand.",
                        name: "Michkel Anegl",
                        role: "Marketing Managment"
                    },
                ]
            }
        }
    }
</script>

<template>
    <section class="px-0">
            <!-- text-container -->
    
            <div class="testimonial-container">
                <div class="section-title-cont text-center">
                    <small class="d-inline-block pb-2 fw-medium">Testimonial</small>
                    <h2 class="fs-1 pb-2"><span class="fw-bold">What</span> People Say</h2>
                    <p>When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper surface</p>
                </div>
        
                <!-- card container with cycle stamp -->
    
                <div class="cards-cont">
                    <div class="row row-cols-4 justify-content-center g-5">
                        <div class="col" v-for="SingleEl in testimonialList">
                            <SingleTestimonial :singleTest="SingleEl"></SingleTestimonial>
                        </div>
                    </div>
                </div>
            </div>

    </section>
</template>

<style lang="scss" scoped>
    @use "../sass/partials/variables";
    @use "../sass/partials/mixins";

    .testimonial-container{
        margin-top: 10rem;

        small{
            color: variables.$over-color-text;
        };

        .cards-cont{
            margin-top: 12rem;


        }

    }



</style>
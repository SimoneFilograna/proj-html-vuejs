<script>
    import CardSpecialHover from "./CardSpecialHover.vue" ;
    export default {
        components:{
            CardSpecialHover,
        },
        data(){
            return{
                CardList: [
                    {
                        img: "../assets/Group-247.png",
                        title: "Data Analysis",
                        info: "When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper"
                    },
                    {
                        img: "../assets/Group-567.png",
                        title: "SEO Optimization",
                        info: "When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper"
                    },
                    {
                        img: "../assets/Group-538.png",
                        title: "Security Data",
                        info: "When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper"
                    },
                    {
                        img: "../assets/Group-566.png",
                        title: "Branding Strategy",
                        info: "When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper"
                    },
                ]
            }
        },
    }
</script>

<template>
    <section class="pt-5">

        <!-- text container side -->

        <div class="upper-container">
            <div class="section-title-cont text-center">
                <small class="d-inline-block pb-2 fw-medium">Our Service</small>
                <h2 class="pb-2"><span class="fw-bold">What</span> We Do</h2>
                <p>When, while the lovely valley teems with vapour around meand the</p>
            </div>
    
            <!-- card container with cycle stamp -->

            <div class="container-fluid">
                <div class="row row-cols-4 align-items-center g-0">
                    <div class="col" v-for="SingleEl in CardList">
                        <CardSpecialHover :cardObj="SingleEl"></CardSpecialHover>
                    </div>
                </div>
            </div>
        </div>

        <!-- lower button  -->

        <div class="lower-button text-center">
            <button type="button" class="btn btn-primary red-button">View All Services</button>
        </div>
    </section>
</template>

<style lang="scss" scoped>
    @use "../sass/partials/variables";
    @use "../sass/partials/mixins";

    small{
        color: variables.$over-color-text;
        font-size: variables.$text-small-size;
    };

    h2{
        font-size: variables.$text-section-h2;
    };

    p{
        font-size: variables.$text-small-size
    }


    .red-button{
        @include mixins.red-button;
        @include mixins.red-shadow;
        font-size: 1.1rem;
        width: 240px;
        padding-top: .9rem;
        padding-bottom: .9rem;
        margin-top: 8rem;
    &:hover{
        @include mixins.blue-hover;
        @include mixins.blue-shadow
    }
    }
</style>
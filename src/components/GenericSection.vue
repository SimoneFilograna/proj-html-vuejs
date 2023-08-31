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
                        info: "hen, while the lovely valley teems with vapour around meand the meridian sun strikes the upper"
                    },
                ]
            }
        },
    }
</script>

<template>
    <section class="pt-5">
        <div class="section-title-cont text-center">
            <small class="d-inline-block pb-2 fw-medium">Our Service</small>
            <h2 class="fs-1 pb-2"><span class="fw-bold">What</span> We Do</h2>
            <p>When, while the lovely valley teems with vapour around meand the</p>
        </div>

        <div class="container">
            <div class="row row-cols-4">
                <div class="col" v-for="SingleEl in CardList">
                    <CardSpecialHover :cardObj="SingleEl"></CardSpecialHover>
                </div>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
    @use "../sass/partials/variables";

    small{
        color: variables.$over-color-text;
    }
</style>
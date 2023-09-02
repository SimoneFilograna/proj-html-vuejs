<script>
    import TopFooter from './TopFooter.vue';

    export default{
        components:{
            TopFooter,
        }
    }
</script>

<template>
    <footer>
        <TopFooter></TopFooter>
    
        <div class="credits d-flex justify-content-between">     
                <div class="copyright">
                    <p>@ 2023 Phlox. All Rights Reserved.</p>
                </div>
                <div class="icon-container text-white d-flex gap-5">
                    <i class="fa-brands fa-instagram"></i>
                    <i class="fa-brands fa-linkedin-in"></i>
                    <i class="fa-brands fa-facebook-f"></i>
                    <i class="fa-brands fa-twitter"></i>
                </div>
        </div>
    </footer>


</template>

<style lang="scss" scoped>
    @use "../sass/partials/mixins";
    @use "../sass/partials/variables";

    footer{
        padding-left: 120px;
        padding-right: 120px;
        padding-bottom: 2rem;
        @include mixins.blue-background;


        .credits{
            border-top: 1px solid variables.$footer-color-text;
            padding-top: 2.5rem;

            p{
                color: variables.$footer-color-text;
            }
        }
    }
</style>
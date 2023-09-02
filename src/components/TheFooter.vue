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
                    <a href="#"><i class="fa-brands fa-instagram"></i></a>
                    <a href="#"><i class="fa-brands fa-linkedin-in"></i></a>
                    <a href="#"><i class="fa-brands fa-facebook-f"></i></a>
                    <a href="#"><i class="fa-brands fa-twitter"></i></a>                                                                           
                </div>
        </div>
    </footer>


</template>

<style lang="scss" scoped>
    @use "../sass/partials/mixins";
    @use "../sass/partials/variables";

    footer{
        margin-top: 17rem;
        padding-left: 130px;
        padding-right: 130px;
        padding-bottom: 2rem;
        @include mixins.blue-background;


        .credits{
            border-top: 1px solid variables.$footer-color-text;
            padding-top: 2.5rem;

            p{
                color: variables.$footer-color-text;
            }

            a{
                color: white;
            
            &:hover{
                color: variables.$over-color-text;
                }    
            }
       
        }
    }
</style>
<script>
    export default{

    }

</script>

<template>
    <section>

        <div class="container double-elements d-flex align-items-center">

            <!-- image container -->

            <div class="container-big-img">
                <img src="../assets/men-data.png" class="big-img" alt="">
            </div>
    
            <!-- text containter -->

            <div class="text-introduce text-white d-flex flex-column gap-3">
                <div class="title">
                    <p>Start Your Project</p>
                    <h2 class="fw-bold">Grow Your Business</h2>
                    <p class="under-para">With Our Strategy</p>
                </div>
                <div class="inner-para">
                    <p class="info pe-5">When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper surface .of the impenetrable foliage of my trees, and but a few stray gleams steal into the inner sanctuary,</p>
                </div>
    
                <!-- button lower -->

                <div class="button-cont">
                    <button type="button" class="btn btn-primary red-button">Try It Now</button>
                    <button type="button" class="btn btn-primary blue-button">Explore More</button>           
                </div>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
    @use "../sass/partials/variables";
    @use "../sass/partials/mixins";

    section{
        @include mixins.blue-background
    }
    .double-elements{
        margin-top: 6.5rem;
        padding-top: 5rem;
        padding-bottom: 9rem;
        .text-introduce{
            margin-top: 3rem;
            margin-left: 20rem;
            h2{
                font-size: 3.5rem;
            };

            .under-para{
                font-size: 3.5rem;
            }
            
            .inner-para{
                .info{
                    color: variables.$blue-text;        
                };

            }

            .button-cont{
                .red-button{
                    @include mixins.red-button;
                    width: 140px;
                    padding-top: .5rem;
                    padding-bottom: .5rem;
    
                &:hover{
                    @include mixins.blue-hover;
                    @include mixins.blue-shadow;
                }
        
                }
                .blue-button{
                    @include mixins.blue-button;
                    width: 140px;
                    padding-top: .5rem;
                    padding-bottom: .5rem;
                    margin-left: 1rem;
    
                &:hover{
                    @include mixins.red-hover;
                    @include mixins.red-shadow;
                    }
                }
            }
    
        };
        
        .container-big-img{
            width: 1200px;
            background-image: url(../assets/nemoodar.png);
            background-position: 0 -20px;
            background-size: contain;
            background-repeat: no-repeat;
            .big-img{
                width: 400px;
                margin-left: 3rem;
            }
        }

    }
</style>
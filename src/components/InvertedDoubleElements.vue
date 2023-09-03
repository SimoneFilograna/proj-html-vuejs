<script>
    export default{

    }

</script>

<template>
    <section>

        <div class="double-elements">

    <!-- image container -->

            <div class="container-big-img">
                <img src="../assets/men-data.png" class="big-img" alt="">
            </div>
    
    <!-- text containter -->

            <div class="text-introduce text-white d-flex flex-column gap-3">
                <div class="title">
                    <p class="mb-5">Start Your Project</p>
                    <h2 class="fw-bold">Grow Your Business</h2>
                    <p class="under-para">With Our Strategy</p>
                </div>
                <div class="inner-para">
                    <p class="info pe-5">When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper surface .of the impenetrable foliage of my trees, and but a few stray gleams steal into the inner sanctuary,</p>
                </div>
    
                <!-- button lower -->

                <div class="button-cont">
                    <button type="button" class="btn btn-primary red-button me-3">Try It Now</button>
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
        display: flex;
        align-items: center;
        gap: 10rem;
        margin-top: 6.5rem;
        padding-top: 10rem;
        padding-bottom: 12rem;
        .text-introduce{
            padding-left: 5rem;
            margin-top: 3rem;
            h2{
                font-size: 4.2rem;
            };

            p{
                font-size: variables.$text-small-size;   
            }

            .under-para{
                font-size: 4.2rem;
            }
            
            .inner-para{
                .info{
                    color: variables.$blue-text;  
                    font-size: variables.$text-small-size;      
                };

            }

            .button-cont{

                margin-top: 2rem;
                .red-button{
                    @include mixins.red-button;
                    width: 180px;
                    padding-top: .8rem;
                    padding-bottom: .8rem;
                    font-size: 1.1rem;
    
                &:hover{
                    @include mixins.blue-hover;
                    @include mixins.blue-shadow;
                }
        
                }
                .blue-button{
                    @include mixins.blue-button;
                    width: 180px;
                    padding-top: .8rem;
                    padding-bottom: .8rem;
                    margin-left: 1rem;
                    font-size: 1.1rem;
    
                &:hover{
                    @include mixins.red-hover;
                    @include mixins.red-shadow;
                    }
                }
            }
    
        };
        
        .container-big-img{
            width: 90%;
            padding-left: 5rem;
            background-image: url(../assets/nemoodar.png);
            background-position: 0 -20px;
            background-size: contain;
            background-repeat: no-repeat;
            .big-img{
                object-fit: contain;
                margin-left: 3rem;
            }
        }

    }
</style>
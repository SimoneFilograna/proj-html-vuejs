<script>
    export default{

    }

</script>

<template>
    <div class="double-elements d-flex align-items-center gap-4">

        <!-- text-container jumbo -->

        <div class="text-introduce text-white d-flex flex-column gap-5">
            <div class="title">
                <h2 class="fw-bold">Business Planning</h2>
                <h2>Digital Technology</h2>
                <h2 class="fw-bold">Modern Solution!</h2>
            </div>
            <div>
                <p class="info">When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper surface . </p>
            </div>

            <!-- lower button in text container -->

            <div class="button-cont">
                <button type="button" class="btn btn-primary red-button me-3" >Try It Now</button>
                <button type="button" class="btn btn-primary blue-button">Explore More</button>           
            </div>
        </div>

            <!-- right side img -->

        <div>
            <img src="../assets/header.png" class="big-img" alt="">
        </div>
    </div>
</template>

<style lang="scss" scoped>
    @use "../sass/partials/variables";
    @use "../sass/partials/mixins";

    .double-elements{
        padding-top: 5rem;
        padding-bottom: 7rem;
        .text-introduce{
            h2{
                font-size: 4.2rem;
            }
            
            .info{
                width: 60%;
                color: variables.$blue-text; 
                font-size: 1.1rem           
            };

            .button-cont{
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
    
        .big-img{
            width: 100%;
            margin-left: 3rem;
        }

    }
</style>
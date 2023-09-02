<script>
    export default{      
    }
</script>
<template>
    <section class="position-relative">
        <!-- text containter -->
        <div class="section-title-cont text-center text-white">
            <small class="d-inline-block pb-4 fw-medium">Price List</small>
            <h2 class="fs-1 pb-3"><span class="fw-bold">Our</span> Pricing</h2>
            <p>When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper surface.</p>
        </div>

        <!-- basic cards -->

        <div class="big-card-container">
            <div class="row row-cols-3">

                <!-- card 1 -->

                <div class="col">
                    <div class="card text-center h-100" >
                        <div class="container-number position-relative">
                            <p class="background-numb">40</p>
                        </div>
                        <div class="card-body position-relative">
                            <h2 class="card-text">Designing</h2>
                            <p>PROCESS</p>
                            <div class="price-container">
                                <span>$</span>
                                <p class="display-1">40</p>
                                <small>Per Month</small>
                            </div>
                            <div class="info">
                                <p><strong>Creative</strong> Designed Enabled</p>
                                <p><strong>Vibrant</strong> Color Usage</p>
                                <p><strong>Eye</strong> Catching Design</p>
                                <p><strong>Extreme</strong> Typografy</p>
                                <p><strong>Exceptional</strong> Design</p>
                            </div>

                            <button type="button" class="btn btn-primary red-button px-3">
                                <span class="d-inline-block pe-4">Order Now</span>
                                <i class="fa-solid fa-arrow-right"></i>
                            </button>
                        </div>
                    </div>
                </div>

                
                <!-- card-2 -->

                <div class="col">
                    <div class="card text-center h-100 mid-card">
                        <div class="container-number position-relative">
                            <p class="background-numb">60</p>
                        </div>
                        <div class="card-body position-relative">
                            <h2 class="card-text">Developing</h2>
                            <p>PRODUCT</p>
                            <div class="price-container">
                                <span>$</span>
                                <p class="display-1">60</p>
                                <small>Per Month</small>
                            </div>
                            <div class="info">
                                <p><strong>Creative</strong> Designed Enabled</p>
                                <p><strong>Vibrant</strong> Color Usage</p>
                                <p><strong>Eye</strong> Catching Design</p>
                                <p><strong>Extreme</strong> Typografy</p>
                                <p><strong>Exceptional</strong> Design</p>
                            </div>

                            <button type="button" class="btn btn-primary mid-button px-3">
                                <span class="d-inline-block pe-4">Order Now</span>
                                <i class="fa-solid fa-arrow-right"></i>
                            </button>
                        </div>
                    </div>
                </div>
                
                <!-- card-3 -->
                
                <div class="col">
                    <div class="card text-center h-100" >
                        <div class="container-number position-relative">
                            <span class="background-numb">80</span>
                        </div>
                        <div class="card-body position-relative">
                            <h2 class="card-text">Supporting</h2>
                            <p class="fw-bold">CLIENTS</p>
                            <div class="price-container">
                                <span>$</span>
                                <p class="display-1">40</p>
                                <small>Per Month</small>
                            </div>
                            <div class="info">
                                <p><strong>Creative</strong> Designed Enabled</p>
                                <p><strong>Vibrant</strong> Color Usage</p>
                                <p><strong>Eye</strong> Catching Design</p>
                                <p><strong>Extreme</strong> Typografy</p>
                                <p><strong>Exceptional</strong> Design</p>
                            </div>

                            <button type="button" class="btn btn-primary red-button px-3">
                                <span class="d-inline-block pe-4">Order Now</span>
                                <i class="fa-solid fa-arrow-right"></i>
                            </button>
                        </div>
                    </div>
                </div>

            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
    @use "../sass/partials/mixins";
    @use "../sass/partials/variables";

    section{
        margin-top: 7rem;
        @include mixins.blue-background;
        height: 700px;

        .section-title-cont{
           padding-top: 6rem;

           small{
                color: variables.$over-color-text;
            };
        }

        .big-card-container{
            width: 85%;
            position: absolute;
            bottom: -120%;
            left: 50%;
            transform: translate(-50%, -50%);
            
            .card{
                border: 0;
                border-radius: 30px;
                box-shadow: 0px 0px 10px rgb(233, 233, 233);
                .background-numb{
                    font-weight: 700;
                    position: absolute;
                    top: -100px;
                    right: -10px;
                    font-size: 18rem;
                    color: rgba($color: lightgray, $alpha: .6);
                }
                .card-body{
    
                    h2{
                        font-size: 3rem;
                        font-weight: 700;
                    }
                    .price-container{
                        position: relative;
        
                        span{
                            position: absolute;
                            top: 2.5rem;
                            left: 11rem;
                        }
        
                        p{
                            padding-top: 2rem;
                            font-size: 8rem;
                            font-weight: 600;
                        }
                        
                        small{
                            position: absolute;
                            bottom: -10px;
                            right: 200px;
                        }
                    };
    
                    .info{
                        padding-top: 2.5rem;
                        font-size: 1.1rem;
                        p{
                            padding-top: .5rem;
                        }
                    }
                }

                .red-button{
                    margin-top: 3rem;
                    @include mixins.red-button;
                    @include mixins.red-shadow;
                    font-size: 1.5rem;
                    margin-bottom: 5rem;

                &:hover{
                    @include mixins.blue-button;
                    @include mixins.blue-shadow
                    }
                };               
            };

            .mid-card{
                    @include mixins.red-hover;
                    color: white;
                
                    .mid-button{
                        @include mixins.blue-button;
                        margin-top: 3rem;
                        font-size: 1.5rem;
                        background: white;
                        color: variables.$over-color-text;
                    }
                }
        }

    }
</style>
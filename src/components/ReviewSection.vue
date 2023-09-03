<script>
    export default{

    }
</script>

<template>
    <section>
        <div class="review-container">
            <div class="section-title-cont text-center">
                <small class="d-inline-block pb-3 fw-medium">Blog</small>
                <h2 class="pb-2"><span class="fw-bold">Latest</span> Post</h2>
                <p>When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper surface</p>
            </div>
    
            <div class="card-container">
                <div class="row g-5">

                    <!-- x2col card -->

                    <div class="col-6 position-relative">
                        <div class="filter-box"></div>
                        <div class="h-100 text-white special-img-card d-flex align-items-end p-5 gap-5">

                            <div class="card-body d-flex flex-column text-box position-relative gap-4">
                                <p class="card-text">April 21, 2019 &bull; by Paul</p>
                                <h5 class="card-title fw-bold fs-4">Clearing Corporations get SEBI not to invest in overnight funds</h5>
                                <p class="card-text"> When, while the lovely valley teems with vapur aroud me, and the meridian s ...</p>
                            </div>

                            <div class="button position-relative">
                                <button type="button" class="btn btn-light mt-auto">Read More</button>
                            </div>
                        </div>
                    </div>

                    <!-- col-card -->

                    <div class="col-3">
                        <div class="card h-100 small-card text-white">
                            <div class="card-body d-flex flex-column mt-5 gap-5 px-5 pb-5">
                                <p class="card-text">April 21, 2019 &bull; by Paul</p>
                                <h5 class="card-title fw-bold fs-4">Clearing Corporations get SEBI not to invest in overnight funds</h5>
                                <p class="card-text"> When, while the lovely valley teems with vapur aroud me, and the meridian s ...</p>
                                <button type="button" class="btn btn-light mt-auto">Read More</button>
                            </div>
                        </div>
                    </div>

                    <!-- last-col-card -->

                    <div class="col-3">
                        <div class="card h-100 small-card text-white" >
                            <div class="card-body d-flex flex-column mt-5 gap-5 px-5 pb-5">
                                <p class="card-text">April 21, 2019 &bull; by Paul</p>
                                <h5 class="card-title fw-bold fs-4">Shabnam Dhillion, wife of RSSB chief Gurinder Dhillion, passes away in London</h5>
                                <p class="card-text"> When, while the lovely valley teems with vapur aroud me, and the meridian s ...</p>
                                <button type="button" class="btn btn-light mt-auto">Read More</button>
                            </div>
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

    .review-container{
        margin-top: 40rem;

        .section-title-cont{
            small{
                color: variables.$over-color-text;
                font-size: variables.$text-small-size;
            };
            
            h2{
                font-size: variables.$text-section-h2;
            };

            p{
                font-size: variables.$text-small-size; 
            }
        }

        .card-container{
            padding-top: 6rem;

            .filter-box{
                    
                    position: absolute;
                    border-radius: 30px;
                    width: 95%;
                    height: 100%;
                    background-color: rgba(0, 0, 0, 0.349);
                }
            .special-img-card{
                background-image: url(../assets/headway-537308-unsplash-1380x703.jpg);
                border-radius: 30px;


                .btn{
                    width: 180px;
                    border-radius: 40px;
                    padding-top: .8rem;
                    padding-bottom: .8rem;
                    border: 0;

                &:hover{
                    @include mixins.red-hover;
                    }
                }   

            }
            .card{
                border-radius: 30px;
                @include mixins.blue-background;
                border: 0;

                .btn{
                    width: 180px;
                    border-radius: 40px;
                    padding-top: .8rem;
                    padding-bottom: .8rem;
                    border: 0;

                &:hover{
                    @include mixins.red-hover;
                    }
                }   
            }
        }
    }
</style>
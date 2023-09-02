<script>
    export default{

    }
</script>

<template>
    <section>
        <div class="review-container">
            <div class="section-title-cont text-center">
                <small class="d-inline-block pb-2 fw-medium">Blog</small>
                <h2 class="fs-1 pb-2"><span class="fw-bold">Latest</span> Post</h2>
                <p>When, while the lovely valley teems with vapour around meand the meridian sun strikes the upper surface</p>
            </div>
    
            <div class="card-container">
                <div class="row g-5">

                    <!-- x2col card -->

                    <div class="col-6">
                        <div class="card h-100 text-white">                  
                            <img src="../assets/headway-537308-unsplash-1380x703.jpg" class="card-img" alt="">
                            <div class="card-img-overlay d-flex flex-column h-100 ps-5">
                                <p class="card-text mt-auto">April 21, 2019 &bull; by Paul</p>
                                <h5 class="card-title">Amazon gets CCI nod to acquire 49% stake in</h5>
                                <div class="d-flex justify-content-between align-items-baseline">
                                    <p>When, while the lovely valley teems with vapur aroud me, and the meridian s ...</p>
                                    <button type="button" class="btn btn-light">Read More</button>
                                </div>
                            </div>
                        </div>
                    </div>

                    <!-- col-card -->

                    <div class="col-3">
                        <div class="card h-100 small-card text-white">
                            <div class="card-body d-flex flex-column mt-5 gap-5 px-5">
                                <p class="card-text">April 21, 2019 &bull; by Paul</p>
                                <h5 class="card-title">Clearing Corporations get SEBI not to invest in overnight funds</h5>
                                <p class="card-text"> When, while the lovely valley teems with vapur aroud me, and the meridian s ...</p>
                                <button type="button" class="btn btn-light mt-auto">Read More</button>
                            </div>
                        </div>
                    </div>

                    <!-- last-col-card -->

                    <div class="col-3">
                        <div class="card h-100 small-card text-white" >
                            <div class="card-body d-flex flex-column mt-5 gap-5 px-5">
                                <p class="card-text">April 21, 2019 &bull; by Paul</p>
                                <h5 class="card-title">Shabnam Dhillion, wife of RSSB chief Gurinder Dhillion, passes away in London</h5>
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
        margin-top: 38rem;

        .section-title-cont{
            small{
                color: variables.$over-color-text;
            }    
        }

        .card-container{
            padding-top: 6rem;
            .card{
                border-radius: 30px;
                @include mixins.blue-background;
                border: 0;
                .card-img{
                    border-radius: 30px;
                    object-fit: contain;
                }
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
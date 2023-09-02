<script>
    export default{

    }
</script>

<template>
    <div class="sub-container text-white d-flex align-items-center justify-content-between">
        <div class="offer-text">
            <h2 class="pb-1 display-4 fw-bold">We Offer Awesome Services</h2>
            <p>When, while lovely valley teems with vapour around meand meridian sun strikes the upper surface.</p>
        </div>

        <div class="input-container">
            <input type="email" class="email-cont form-control" placeholder="Enter Your Email Address" >
            <button type="button" class="btn btn-primary">Subscribe</button>
        </div>
    </div>
</template>

<style lang="scss" scoped>
    @use "../sass/partials/mixins";
    @use "../sass/partials/variables";

    .sub-container{
        padding: 5.5rem 3.5rem;
        @include mixins.red-hover;
        border-radius: 30px;
        .input-container{
            position: relative;
            width: 40%;

            .btn{
                font-size: 1.1rem;
                @include mixins.blue-button;
                position: absolute;
                right: 1%;
                top: 13%;
                padding: 1rem;
                width: 30%;

            &:hover{
                @include mixins.red-hover
                }
            }

            .email-cont{
                font-size: 1.4rem;
                font-weight: 100;
                border-radius: 45px;
                padding: 1.2rem 2rem;
            }

        }
    }
</style>
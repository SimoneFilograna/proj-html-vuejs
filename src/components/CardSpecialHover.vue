<script>
    export default{
        props:{
            cardObj:{
                type: Object,
                required: true,
            }
        },
        methods:{
            getImg: function(img){
                return new URL(img, import.meta.url).href
            }
        }
    }
</script>

<template>
    <div class="text-card text-center card border-0">
        <div class="img-container">
            <img :src="getImg(cardObj.img)" class="card-img" alt="">
        </div>

        <div class="text-container px-5 pt-2 card-body">
            <h3 class="fw-bold card-text pb-4">{{ cardObj.title }}</h3>
            <p class="card-text px-3">{{ cardObj.info }}</p>
        </div>

        <div class="button-div">
            <a href="#" class="text-decoration-none text-white">
                <i class="fa-solid fa-arrow-right arrow-custom"></i>
            </a>
        </div>
    </div>
</template>

<style lang="scss" scoped>
    @use "../sass/partials/mixins";
    @use "../sass/partials/variables";
    .text-card{
        padding: 2rem;
        position: relative;
        padding-top: 9rem;
        padding-bottom: 4rem;
        border-radius: 1.5rem;
        margin-top: 13rem;
        transition: all .8s linear;

    &:hover .button-div{
        opacity: 1;
    };

    &:hover{
        @include mixins.blue-background;
        color: rgb(255, 255, 255);
    };

    &:hover .card-img{
        background-color: rgb(255, 255, 255);
        box-shadow: 0px -3px 8px 1px lightgrey;
        
    }

        .img-container{
            position: absolute;
            top: 0;
            left: 50%;
            transform: translate(-50%, -50%);
            

            .card-img{
                padding: 2rem;
                width: 230px;
                aspect-ratio: 1/1;
                object-fit: cover;
                border-radius: 1.5rem;
                object-fit: contain
            }
        };

        .button-div{
            opacity: 0;
            position: absolute;
            bottom: 0;
            left: 50%;
            transform: translate(-50%, 50%);
            .arrow-custom{
                @include mixins.red-hover;
                padding: 1.8rem;
                border-radius: 50%;
            }
        };

        .text-container{
            font-size: variables.$text-small-size;
        }

    }


</style>
<script>

    import StarRating from 'vue-star-rating'

    export default{
        components:{
            StarRating,
        },
        props:{
            singleTest: {
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
        <div class="card text-center d-fle flex-column gap-4 position-relative">

            <div class="img-container">
                <img :src="getImg(singleTest.photo)" class="card-img-top" alt="...">
            </div>

            <div class="stars-container d-flex justify-content-center">
                <star-rating :rating="3"
                             border-color="#de4a6c"
                             :star-size="18"
                             :increment="0.5"
                             active-color="#de4a6c"
                             inactive-color="#FFFFFF"
                             :border-width="1"
                             :show-rating="false"
                             :read-only="true">
                </star-rating>
            </div>

            <div class="card-body">
                <p class="card-text">{{ singleTest.comment }}</p>
                <h6 class="card-text fw-bold fs-5 pt-3">{{ singleTest.name  }}</h6>
                <p class="card-text">{{ singleTest.role }}</p>
            </div>
        </div>


</template>

<style lang="scss" scoped>
    .card{
        border: 0;
        border-radius: 30px;
        padding-bottom: .5rem;
        transition: box-shadow .5s linear;
    
    &:hover{
        box-shadow: 0px -3px 60px 30px rgb(233, 233, 233);
    }

        .img-container{
            width: 120px;
            margin: auto;
            border-radius: 50%;
            border: 5px solid #de4a6c;
            position: absolute;
            top: 0;
            left: 50%;
            transform: translate(-50%, -50%);
        };

        .stars-container{
            margin-top: 2rem;
            padding-top: 5rem;
            padding-bottom: 2rem;
            background-image: url(../assets/bg-mini-card.png);
            background-repeat: no-repeat;
            background-position: 55% 80%;
        }


        .card-body{
            font-size: 1.2rem;
        };
    }
</style>
<script>
    export default{
        props:{
            carouselObj:{
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
    <div class="card h-100 d-flex flex-column me-4" :key="carouselObj.id">
        <img :src="getImg(carouselObj.img)" class="card-img-top" :alt="`card n${carouselObj.id}`">
        <div class="card-body d-flex justify-content-between">
            <span class="card-text">{{ carouselObj.title }}</span>
            <small>{{ carouselObj.info }}</small>
        </div>
    </div>
</template>

<style lang="scss" scoped>
    @use "../sass/partials/mixins";
    .card{
        width: 550px;
        border-radius: 35px;
        border: 1px;
        box-shadow: 0px 0px 30px -25px rgb(88, 88, 88);

    &:hover {
        @include mixins.red-hover;
    };

    &:hover .card-body{
        color: white;
    }

        img{
            border-radius: 30px;
            border-color: transparent;
        }

        .card-body{
            border-radius: 35px;
            margin-top: 1rem;
            margin-bottom: .8rem;
        }
    }

</style>
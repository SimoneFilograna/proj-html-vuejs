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
    <div class="card h-100 d-flex flex-column " :key="carouselObj.id">
        <img :src="getImg(carouselObj.img)" class="card-img-top" :alt="`card n${carouselObj.id}`">
        <div class="card-body d-flex justify-content-between">
            <span class="card-text">{{ carouselObj.title }}</span>
            <small>{{ carouselObj.info }}</small>
        </div>
    </div>
</template>

<style lang="scss" scoped>
    .card{
        width: 500px;
    }
</style>